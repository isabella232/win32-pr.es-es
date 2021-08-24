---
description: Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe de eventos.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtención de un GUID de clase y proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914355"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Obtención de un GUID de clase y proveedor

Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe de eventos.

Si usa la herramienta Uuidgen.exe, use la opción -d para crear una macro DEFINE GUID C, como se muestra \_ en el ejemplo siguiente. Para obtener información sobre el uso de Uuidgen.exe herramienta, use el método -? . Si usa la macro DEFINE GUID C para definir el GUID, debe incluir \_ define INITGUID antes de las definiciones de GUID, como se muestra \# en el ejemplo siguiente.

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

Microsoft Windows Software Development Kit (SDK) y Microsoft Visual Studio la herramienta Guidgen.exe software. La Guidgen.exe tiene una interfaz de usuario que le permite seleccionar entre varios formatos. Debe usar el formato que crea un GUID constante estático, como se muestra en el ejemplo siguiente.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



