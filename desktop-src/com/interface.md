---
title: Interfaz (COM)
description: Una entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Interfaz de la clave del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714524"
---
# <a name="interface-com"></a><span data-ttu-id="0dd7c-104">Interfaz (COM)</span><span class="sxs-lookup"><span data-stu-id="0dd7c-104">Interface (COM)</span></span>

<span data-ttu-id="0dd7c-105">Una entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.</span><span class="sxs-lookup"><span data-stu-id="0dd7c-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0dd7c-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0dd7c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="0dd7c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dd7c-107">Remarks</span></span>

<span data-ttu-id="0dd7c-108">Si el nombre de una interfaz no está presente en esta lista, la interfaz nunca puede ser compatible con una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0dd7c-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dd7c-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0dd7c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dd7c-110">Clave de interfaz</span><span class="sxs-lookup"><span data-stu-id="0dd7c-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




