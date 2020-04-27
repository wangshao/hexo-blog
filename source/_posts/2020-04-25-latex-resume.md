---
title: 试用 OverLeaf LaTex 编辑器
date: 2020-04-25 16:00:51
tags: LaTeX
---
试用了下用 [OverLeaf](https://www.overleaf.com/project/) 提供的 LaTex 在线编辑器，用的还是比较舒爽的，毕竟不用装 MacTex 那个 3.3G 的安装包。在线编译的速度也挺快，还有语法检查。
用自己的简历做了个例子，东西不多，简单干净，当然也可以玩点花活，比如两列简历，比如饼图线图云图一些可视化的 package。暂时没有时间去搞这些，对自己的审美还是有点怀疑，怕搞的花里胡哨的。

贴一下简单的源码
```
% !TEX TS-program = xelatex
% !TEX encoding = UTF-8 Unicode
% !Mode:: "TeX:UTF-8"

\documentclass{resume}
\usepackage{zh_CN-Adobefonts_external} % Simplified Chinese Support using external fonts (./fonts/zh_CN-Adobe/)
%\usepackage{zh_CN-Adobefonts_internal} % Simplified Chinese Support using system fonts
\usepackage{linespacing_fix} % disable extra space before next section
\usepackage{cite}
\usepackage{graphicx}
\usepackage{tabu}
\usepackage{multirow}

\begin{document}
\pagenumbering{gobble} % suppress displaying page number

% \name{王绍}\textperiodcentered\ 

\Large{
  \begin{tabu}{ l l}
   \multirow{2}{*}{\includegraphics[width=0.6in]{wechat}} & \scshape{王绍} \\
    & \github[wangshao]{https://github.com/wangshao} \textperiodcentered\ \linkedin[Shao Wang]{https://www.linkedin.com/in/shao-wang-9591a623/} \\
    & \email{waangshao@outlook.com} \textperiodcentered\ \faWechat{ bartallen} \textperiodcentered\ \phone{(+86)18017545245}
  \end{tabu}
}
% \basicInfo{
%   \email{waangshao@outlook.com} \textperiodcentered\ 
%   \phone{(+86) 18017545245} \textperiodcentered\ 
%   \linkedin[Shao Wang]{https://www.linkedin.com/in/shao-wang-9591a623/}} \textperiodcentered\ 
%   \github[wangshao]{https://github.com/wangshao} \textperiodcentered\ 
%   \faWechat[bartallen] \textperiodcentered\ 
 
\section{\faGraduationCap\  教育背景}
\datedsubsection{\textbf{University of Michigan}, Ann Arbor, United States}{2010 -- 2013}
\textit{Bachelor of Science}\ Electrical Engineering
\datedsubsection{\textbf{上海交通大学}, 上海}{2008 -- 2012}
\textit{学士}\ 电子与计算机工程


\section{\faUsers\ 工作经历}
\datedsubsection{\textbf{北京逐风科技有线公司} 北京}{2016年4月 -- 现在}
\role{全职 Java 研发工程师}
负责公司产品软件架构开发与维护
\begin{itemize}
  \item 为公司搭建基于 Jenkins, Nexus，docker registry 的开发集成环境
  \item 业务代码开发，系统运行统计信息收集，运行时调优
  \item 负责部分客户线上运维工作，私有化部署，线上问题解决
  \item 优化 Kafka Connect Rebalance 逻辑
  \item 调研并应用 MySQL Binlog，Postgres Replication Slot SqlServer ChangeTracking 等实时增量获取
  \item 开发产品任务流功能
  \item 开源框架 Flink，Kubernetes, Kafka 调研以及应用
\end{itemize}

\datedsubsection{\textbf{普华永道信息技术有限公司} 上海}{2016年1月 -- 2016年4月}
\role{全职 Android 开发工程师}

\datedsubsection{\textbf{Kaiser Permanente} Dublin, California, United States}{2014年6月 -- 2015年8月}
\role{全职 Android 开发工程师}
负责提供给 Kaiser Permanente 医院用户 Android APP 的开发与维护
\begin{itemize}
  \item 修复了连接未正常关闭导致文件描述符耗尽的 bug
\end{itemize}

\datedsubsection{\textbf{2RedBeans} Dublin, California, United States}{2013年9月 -- 2014年1月}
\role{实习前端开发工程师}
开发网站前端部分组件
\begin{itemize}
  \item 实现图片走马灯效果
  \item 实现无限下拉功能
\end{itemize}
% Reference Test
%\datedsubsection{\textbf{Paper Title\cite{zaharia2012resilient}}}{May. 2015}
%An xxx optimized for xxx\cite{verma2015large}
%\begin{itemize}
%  \item main contribution
%\end{itemize}

\section{\faCogs\ 技能}
% increase linespacing [parsep=0.5ex]
\begin{itemize}[parsep=0.5ex]
  \item 主力语言: JAVA 辅助语言: Bash, Python, Golang
  \item 框架: Kafka, Redis, Spring, MyBatis, 
  \item 平台: Linux, OsX
  \item 语言：英语 - 熟练 日语 - 入门
\end{itemize}

% \section{\faInfo\ 其他}
% % increase linespacing [parsep=0.5ex]
% \begin{itemize}[parsep=0.5ex]
%   \item 英语 - 熟练(TOEFL 106)
%   \item 日语 - 入门
% \end{itemize}

%% Reference
%\newpage
%\bibliographystyle{IEEETran}
%\bibliography{mycite}
\end{document}

```


