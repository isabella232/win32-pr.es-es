---
title: Archivo make de ejemplo asincrónico
description: El siguiente es el archivo make de la aplicación de ejemplo asincrónica.
ms.assetid: 5d5b5578-6a2e-4311-9bf7-9b7818eb23ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613dd67ab66819bd7f717ddc282ced1de63eff87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903237"
---
# <a name="asynchronous-example-makefile"></a><span data-ttu-id="22021-103">Archivo make de ejemplo asincrónico</span><span class="sxs-lookup"><span data-stu-id="22021-103">Asynchronous Example Makefile</span></span>

<span data-ttu-id="22021-104">El siguiente es el archivo make de la [aplicación de ejemplo asincrónica](asynchronous-example-application.md).</span><span class="sxs-lookup"><span data-stu-id="22021-104">The following is the makefile for the [asynchronous example application](asynchronous-example-application.md).</span></span>

``` syntax
#----- Include the SDK's WIN32.MAK to pick up defines-------------------
!include <win32.mak>

all:    $(OUTDIR) $(OUTDIR)\async.exe 

$(OUTDIR)\async.exe:     $(OUTDIR)\async.obj
    $(link) $(ldebug) /OUT:$(OUTDIR)\async.exe $(conlflags) /PDB:$(OUTDIR)\async.pdb /MACHINE:$(CPU) $(OUTDIR)\async.obj wininet.lib $(baselibs)

$(OUTDIR)\async.obj:    async.c
    $(cc) $(cflags) $(cdebug) $(cvars) /EHsc /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" /D"_CONSOLE" /D"UNICODE" /D"_UNICODE" async.c
        
#----- If OUTDIR does not exist, then create directory
$(OUTDIR) :
    if not exist "$(OUTDIR)/$(NULL)" mkdir $(OUTDIR)

clean:
     $(CLEANUP)
```

 

 




