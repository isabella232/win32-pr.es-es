---
description: ICE76 comprueba el uso del catálogo SFP (WFP) dentro de Windows Installer paquetes para Windows me. Esta ICE también comprueba que ningún archivo de la tabla BindImage hace referencia a los catálogos SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652466"
---
# <a name="ice76"></a>ICE76

ICE76 comprueba el uso del catálogo SFP (WFP) dentro de Windows Installer paquetes para Windows me. Esta ICE también comprueba que ningún archivo de la [tabla](bindimage-table.md) BindImage hace referencia a los catálogos SFP.

La protección de archivos de Windows requiere una coincidencia exacta entre el archivo y la firma incrustada en el archivo de catálogo. Los archivos que hacen referencia a un catálogo SFP no deben aparecer en la tabla BindImage porque el efecto de la [acción BindImage](bindimage-action.md) en estos archivos difiere entre los equipos. Los archivos a los que hacen referencia los catálogos SFP deben encontrarse en componentes permanentes o instalados localmente.

## <a name="result"></a>Resultado

ICE76 publica un error para cada archivo de la [tabla BindImage](bindimage-table.md) que también está en la [tabla FileSFPCatalog](filesfpcatalog-table.md).

ICE76 genera un error si un archivo de la tabla FileSFPCatalog pertenece a un componente con cualquiera de los siguientes elementos true:

-   **msidbComponentAttributesPermanent** no se establece en la columna Attributes de la [tabla Component](component-table.md).
-   **msidbComponentAttributesSourceOnly** se establece en la columna Attributes de la tabla Component.
-   **msidbAttributesOptional** se establece en la columna Attributes de la tabla Component.

## <a name="example"></a>Ejemplo

ICE76 notifica el siguiente error para el ejemplo:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Tabla FileSFPCatalog](filesfpcatalog-table.md) (parcial)



| Archivo\_ | SFPCatalog\_ |
|--------|--------------|
| Archivo1  | Catalog1.Cat |



 

[Tabla BindImage](bindimage-table.md) (parcial)



| Archivo\_ |
|--------|
| Archivo1  |



 

Para corregir esto, no escriba ningún archivo que haga referencia a los catálogos de SFP en la tabla BindImage.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla BindImage](bindimage-table.md)
</dt> <dt>

[Tabla de componentes](component-table.md)
</dt> <dt>

[Tabla FileSFPCatalog](filesfpcatalog-table.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



