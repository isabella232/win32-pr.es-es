---
title: modificador/version_stamp
description: El \_ modificador de marca/version suprime la generación de macros que especifican el número de versión mínimo necesario del archivo de encabezado RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp modificador MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685637"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="a2cc8-104">\_cambio de marca/version</span><span class="sxs-lookup"><span data-stu-id="a2cc8-104">/version\_stamp switch</span></span>

<span data-ttu-id="a2cc8-105">El modificador de **\_ marca/version** suprime la generación de macros que especifican el número de versión mínimo necesario del archivo de encabezado RPC, Rpcndr. h.</span><span class="sxs-lookup"><span data-stu-id="a2cc8-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="a2cc8-106">Las nuevas características de MIDL pueden requerir definiciones adicionales para compilar el código auxiliar correctamente, por lo que el código auxiliar tiene macros que comprueban la compatibilidad entre los archivos binarios MIDL y el entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="a2cc8-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="a2cc8-107">Es posible que tenga que usar este modificador si mueve MIDL a un entorno de compilación diferente del que instaló por primera vez los archivos binarios de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a2cc8-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="a2cc8-108">Tenga en cuenta que no se admite la combinación de entornos de compilación.</span><span class="sxs-lookup"><span data-stu-id="a2cc8-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="a2cc8-109">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="a2cc8-109">Switch Options</span></span>

<span data-ttu-id="a2cc8-110">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2cc8-110">This switch has no parameters.</span></span>

 

 




