---
description: ICE74 comprueba que la propiedad FASTOEM no se ha creado en la tabla de propiedades.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652479"
---
# <a name="ice74"></a>ICE74

ICE74 comprueba que la propiedad [**FASTOEM**](fastoem.md) no se ha creado en la tabla de [propiedades](property-table.md).

La propiedad [**FASTOEM**](fastoem.md) permite a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones por primera vez. No se puede usar después de la primera instalación. La propiedad **FASTOEM** no se debe crear en la tabla de propiedades porque interfiere con las instalaciones posteriores para el mantenimiento, la eliminación o la reparación de la aplicación.

ICE74 también comprueba que la propiedad [**UpgradeCode**](upgradecode.md) se crea en la tabla de [propiedades](property-table.md)y que su valor no es un GUID nulo, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Resultado

ICE74 puede exponer los errores siguientes.



| Error ICE74                                                                       | Descripción                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| La propiedad [**FASTOEM**](fastoem.md) no se puede crear en la tabla de propiedades. | La propiedad [**FASTOEM**](fastoem.md) se ha establecido en la tabla de propiedades.                             |
| ' \[ 2 \] ' no es un [**UpgradeCode**](upgradecode.md)válido.                        | Se ha especificado un GUID null para la propiedad [**UpgradeCode**](upgradecode.md) en la tabla de propiedades. |



 

ICE74 puede enviar la siguiente advertencia.



| ADVERTENCIA de ICE74                                                                                                                                                                                             | Descripción                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| La propiedad [**UpgradeCode**](upgradecode.md) no se crea en la tabla de propiedades. Se recomienda encarecidamente que los autores de los paquetes de instalación especifiquen **UpgradeCode** para su aplicación. | La propiedad [**UpgradeCode**](upgradecode.md) no se crea en la tabla de propiedades. |



 

## <a name="example"></a>Ejemplo

ICE74 notifica el siguiente error si se establece la propiedad [**FASTOEM**](fastoem.md) : FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad                   | Value |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Para corregir este error, quite la propiedad [**FASTOEM**](fastoem.md) de la tabla de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**propiedad FASTOEM**](fastoem.md)
</dt> <dt>

[Tabla de propiedades](property-table.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



