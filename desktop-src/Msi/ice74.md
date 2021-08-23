---
description: ICE74 comprueba que la propiedad FASTOEM no se ha escrito en la tabla Property.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3120b0f4cd40acc53a1bcd3623dac33941a7f5da39bc538781e4ffd1d56345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328325"
---
# <a name="ice74"></a>ICE74

ICE74 comprueba que la [**propiedad FASTOEM**](fastoem.md) no se ha escrito en la [tabla Property](property-table.md).

La [**propiedad FASTOEM permite**](fastoem.md) a los OEM reducir el tiempo necesario para instalar aplicaciones Windows Installer por primera vez. No se puede usar después de la primera instalación. La **propiedad FASTOEM** no debe crearse en la tabla Property porque esto interfiere con las instalaciones posteriores para el mantenimiento, la eliminación o la reparación de la aplicación.

ICE74 también comprueba que la propiedad [**UpgradeCode**](upgradecode.md) se ha escrito en la tabla [Property](property-table.md)y que su valor no es un GUID nulo, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Resultado

ICE74 puede publicar los errores siguientes.



| Error ice74                                                                       | Descripción                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| La [**propiedad FASTOEM**](fastoem.md) no se puede crear en la tabla Property. | La [**propiedad FASTOEM**](fastoem.md) se ha establecido en la tabla Property.                             |
| ' \[ 2 \] ' no es un [**upgradeCode válido.**](upgradecode.md)                        | Se ha especificado un GUID nulo para la [**propiedad UpgradeCode**](upgradecode.md) de la tabla Property. |



 

ICE74 puede publicar la advertencia siguiente.



| Advertencia de ICE74                                                                                                                                                                                             | Descripción                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| La [**propiedad UpgradeCode**](upgradecode.md) no se ha escrito en la tabla Property. Se recomienda encarecidamente que los autores de paquetes de instalación especifiquen **un upgradeCode** para su aplicación. | La [**propiedad UpgradeCode**](upgradecode.md) no se ha escrito en la tabla Property. |



 

## <a name="example"></a>Ejemplo

ICE74 notifica el siguiente error si se establece la propiedad [**FASTOEM:**](fastoem.md) FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad                   | Value |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Para corregir este error, quite [**la propiedad FASTOEM**](fastoem.md) de la tabla de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**propiedad FASTOEM**](fastoem.md)
</dt> <dt>

[Tabla de propiedades](property-table.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



