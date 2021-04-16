---
description: Windows Installer se pueden crear paquetes de actualización para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedir que se instale un paquete anterior en una versión más reciente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652579"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Impedir que un paquete antiguo se instale en una versión más reciente

Windows Installer se pueden crear paquetes de actualización para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente. El procedimiento descrito en este tema solo puede impedir las degradaciones que podrían deberse a la ejecución de un paquete de actualización principal. Este procedimiento se basa en la [acción FindRelatedProducts](findrelatedproducts-action.md), que solo se ejecuta durante una instalación por primera vez y no se ejecuta en modo de mantenimiento (reinstalación). Dado que las actualizaciones secundarias se realizan mediante la reinstalación, este procedimiento no se puede usar para determinar si un paquete de actualización menor está intentando degradar una aplicación. Para obtener más información, consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).

**Para evitar que un paquete antiguo se instale en una versión más reciente**

1.  Escriba la propiedad [**UpgradeCode**](upgradecode.md) para el grupo de productos relacionados que pueden ser válidos para recibir esta actualización en la columna UpgradeCode de la [tabla de actualización](upgrade-table.md).
2.  Escriba la marca de bits **msidbUpgradeAttributesOnlyDetect** en la columna atributos de la [tabla de actualización](upgrade-table.md).
3.  Escriba la versión de la actualización proporcionada por este paquete en la columna VersionMin de la [tabla de actualización](upgrade-table.md). Deje en blanco la columna VersionMax.
4.  Escriba el nombre de la propiedad que va a establecer la [acción FindRelatedProducts](findrelatedproducts-action.md) en la columna ActionProperty de la tabla de [actualización](upgrade-table.md).
5.  Agregue la propiedad [**SecureCustomProperties**](securecustomproperties.md) y la propiedad denominada en la columna ActionProperty de la [tabla de actualización](upgrade-table.md) a la [tabla de propiedades](property-table.md).
6.  Agregue un [tipo de acción personalizada 19](custom-action-type-19.md) después de la acción FindRelatedProducts en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Incluya un registro en la [tabla CustomAction](customaction-table.md) para esta acción y escriba el texto que se mostrará en la columna de destino. La acción personalizada tipo 19 está integrada en el instalador, por lo que no hay código que escribir.
7.  Escriba el nombre del ActionProperty en la columna condición del registro en la [tabla InstallExecuteSequence](installexecutesequence-table.md) que contiene el [tipo de acción personalizada 19](custom-action-type-19.md). Esta acción solo se ejecuta cuando la [tabla de actualización](upgrade-table.md) detecta que ya hay instalada una versión más reciente.

    Por ejemplo, un paquete de Windows Installer que actualiza un grupo de productos relacionados con la versión 3,0 puede incluir los registros siguientes en sus tablas de [propiedades](property-table.md) de [actualización](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y. Todos los productos relacionados en el grupo tienen el mismo UpgradeCode, pero el instalador no instala este paquete de actualización si ya hay instalada en el equipo una versión posterior a 3,0. En este caso, el instalador presenta un mensaje de error y se produce un error en la instalación. El paquete de actualización de la versión 3,0 se instala en las versiones 1,0 y 2,0.

    [Actualizar tabla](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos                                | Remove | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1,0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [Tabla CustomAction](customaction-table.md)

    

    | Acción | Tipo | Source | Destino                                 |
    |--------|------|--------|----------------------------------------|
    | CA1    | 19   |        | Ya hay instalada una actualización superior. |

    

     

    [Tabla InstallExecuteSequence](installexecutesequence-table.md)

    

    | Acción              | Condición       | Secuencia |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | CA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Tabla de propiedades](property-table.md)

    

    | Propiedad                                                 | Value                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 



