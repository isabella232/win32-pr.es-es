---
title: ProxyStubClsid
description: Asigna un IID a un CLSID en archivos dll de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valor del registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076127"
---
# <a name="proxystubclsid"></a><span data-ttu-id="6216e-104">ProxyStubClsid</span><span class="sxs-lookup"><span data-stu-id="6216e-104">ProxyStubClsid</span></span>

<span data-ttu-id="6216e-105">Asigna un IID a un CLSID en archivos dll de proxy de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6216e-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6216e-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="6216e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="6216e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6216e-107">Remarks</span></span>

<span data-ttu-id="6216e-108">Se trata de un valor de **reg \_ SZ** que especifica el CLSID para el IID.</span><span class="sxs-lookup"><span data-stu-id="6216e-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="6216e-109">Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 16 bits) para que OLE pueda encontrar el código remoto adecuado para establecer la comunicación entre procesos.</span><span class="sxs-lookup"><span data-stu-id="6216e-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6216e-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6216e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6216e-111">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="6216e-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="6216e-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="6216e-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




