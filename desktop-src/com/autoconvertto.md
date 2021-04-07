---
title: Conversión a
description: Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Convertir en COM clave del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103902994"
---
# <a name="autoconvertto"></a><span data-ttu-id="6f91e-104">Conversión a</span><span class="sxs-lookup"><span data-stu-id="6f91e-104">AutoConvertTo</span></span>

<span data-ttu-id="6f91e-105">Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos.</span><span class="sxs-lookup"><span data-stu-id="6f91e-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6f91e-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="6f91e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="6f91e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f91e-107">Remarks</span></span>

<span data-ttu-id="6f91e-108">Se trata de un valor de **reg \_ SZ** que especifica el identificador de clase del objeto al que se debe convertir el objeto o la clase de objetos especificados.</span><span class="sxs-lookup"><span data-stu-id="6f91e-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="6f91e-109">Esta clave se usa normalmente para convertir automáticamente los archivos creados por una versión anterior de una aplicación a una versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f91e-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f91e-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f91e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f91e-111">**OleDoAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="6f91e-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="6f91e-112">**OleGetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="6f91e-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="6f91e-113">**OleSetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="6f91e-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




