---
description: Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtener un proveedor y un GUID de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985715"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Obtener un proveedor y un GUID de clase

Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe.

Si usa la herramienta Uuidgen.exe, use la opción-d para crear una macro definir \_ GUID C, como se muestra en el ejemplo siguiente. Para obtener información sobre el uso de la herramienta Uuidgen.exe, use el . Si usa la macro definir \_ GUID C para definir el GUID, debe incluir \# define INITGUID antes de las definiciones de GUID, tal como se muestra en el ejemplo siguiente.

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

El kit de desarrollo de software (SDK) de Microsoft Windows y Microsoft Visual Studio incluyen la herramienta Guidgen.exe. La herramienta Guidgen.exe tiene una interfaz de usuario que le permite seleccionar varios formatos. Debe usar el formato que crea un GUID de constante estática, tal como se muestra en el ejemplo siguiente.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



