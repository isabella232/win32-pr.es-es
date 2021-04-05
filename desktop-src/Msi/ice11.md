---
description: ICE11 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte instalaciones simultáneas.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002255"
---
# <a name="ice11"></a>ICE11

ICE11 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.

## <a name="result"></a>Resultado

ICE11 valida la columna de origen de la [tabla CustomAction](customaction-table.md) de acciones personalizadas de instalación simultánea. La columna de origen debe contener un [GUID](guid.md) válido (código de producto MSI).

ICE11 publica un error si la columna de origen de la tabla CustomAction no se creó correctamente para las acciones personalizadas de instalación simultánea.

## <a name="example"></a>Ejemplo

ICE envía los siguientes mensajes de error para el ejemplo que se muestra.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad        | Value                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[Tabla CustomAction](customaction-table.md) (parcial)



| CustomAction | Tipo | Source                                 |
|--------------|------|----------------------------------------|
| CA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Para corregir los errores, en el caso de CA1, no puede realizar una instalación simultánea del "paquete base". Esto daría lugar a una instalación recursiva. Esta entrada se debe quitar o la columna de origen debe cambiarse por un GUID para una MSI anunciada que difiere del GUID del paquete base. En el caso de CA2, haga que todos los caracteres del GUID estén en mayúsculas. Por último, cambie la columna de origen de CA4's para que haga referencia a un GUID válido de una MSI anunciada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalaciones simultáneas](concurrent-installations.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



