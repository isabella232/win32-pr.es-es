---
title: ProxyStubClsid32
description: Asigna un IID a un CLSID en dll de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valor del registro ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359447"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="4bd4e-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="4bd4e-104">ProxyStubClsid32</span></span>

<span data-ttu-id="4bd4e-105">Asigna un IID a un CLSID en dll de proxy de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4bd4e-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4bd4e-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="4bd4e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="4bd4e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bd4e-107">Remarks</span></span>

<span data-ttu-id="4bd4e-108">Se trata de un valor de **reg \_ SZ** que especifica el CLSID para el IID.</span><span class="sxs-lookup"><span data-stu-id="4bd4e-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="4bd4e-109">Se trata de una entrada necesaria, ya que la asignación de IID a CLSID puede ser diferente para las interfaces de 16 bits y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4bd4e-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="4bd4e-110">La asignación de IID a CLSID depende de la forma en que los proxies de interfaz se empaquetan en un conjunto de archivos dll de proxy.</span><span class="sxs-lookup"><span data-stu-id="4bd4e-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="4bd4e-111">Si agrega interfaces, debe usar esta entrada para registrarlas (sistemas de 32 bits) para que OLE pueda encontrar el código remoto adecuado para establecer la comunicación entre procesos.</span><span class="sxs-lookup"><span data-stu-id="4bd4e-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bd4e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bd4e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd4e-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="4bd4e-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="4bd4e-114">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="4bd4e-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="4bd4e-115">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="4bd4e-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 