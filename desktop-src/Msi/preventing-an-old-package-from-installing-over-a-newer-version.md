---
description: Windows Los paquetes de actualización del instalador se pueden crear para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedir que un paquete antiguo se instale en una versión más reciente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161453"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Impedir que un paquete antiguo se instale en una versión más reciente

Windows Los paquetes de actualización del instalador se pueden crear para que las actualizaciones principales no se instalen si un usuario ya tiene instalada una versión más reciente. El procedimiento de este tema solo puede evitar degradaciones que podrían deberse a la ejecución de un paquete de actualización principal. Este procedimiento se basa en la acción [FindRelatedProducts](findrelatedproducts-action.md), que solo se ejecuta durante una instalación por primera vez y no se ejecuta en modo de mantenimiento (reinstalación). Dado que las actualizaciones secundarias se realizan mediante la reinstalación, este procedimiento no se puede usar para determinar si un paquete de actualización secundaria está intentando degradar una aplicación. Para obtener más información, vea [Preparar una aplicación para futuras actualizaciones principales.](preparing-an-application-for-future-major-upgrades.md)

**Para evitar que un paquete antiguo se instale en una versión más reciente**

1.  Escriba la [**propiedad UpgradeCode**](upgradecode.md) del grupo de productos relacionados que pueden ser aptos para recibir esta actualización en la columna UpgradeCode de la [tabla de actualización](upgrade-table.md).
2.  Escriba la **marca de bits msidbUpgradeAttributesOnlyDetect** en la columna Atributos de la [tabla de actualización](upgrade-table.md).
3.  Escriba la versión de la actualización proporcionada por este paquete en la columna VersionMin de la [tabla de actualización](upgrade-table.md). Deje la columna VersionMax en blanco.
4.  Escriba el nombre de la propiedad que va a establecer la acción [FindRelatedProducts](findrelatedproducts-action.md) en la columna ActionProperty de la [tabla de actualización](upgrade-table.md).
5.  Agregue la [**propiedad SecureCustomProperties**](securecustomproperties.md) y la propiedad denominada en la columna ActionProperty de [la tabla de actualización](upgrade-table.md) a la tabla de [propiedades](property-table.md).
6.  Agregue un [tipo de acción personalizada 19](custom-action-type-19.md) después de la acción FindRelatedProducts en la tabla [InstallExecuteSequence](installexecutesequence-table.md). Incluya un registro en la [tabla CustomAction para](customaction-table.md) esta acción y escriba el texto que se mostrará en la columna Destino. La acción personalizada de tipo 19 está integrada en el instalador, por lo que no hay código para escribir.
7.  Escriba el nombre de ActionProperty en la columna Condición del registro en [InstallExecuteSequence Table](installexecutesequence-table.md) que contiene el tipo de acción [personalizada 19.](custom-action-type-19.md) Esto hace que la acción personalizada solo se ejecute cuando la tabla de actualización [detecte](upgrade-table.md) que ya está instalada una versión más reciente.

    Por ejemplo, un paquete de Windows Installer que actualiza un grupo de productos relacionados a la versión 3.0 puede incluir los siguientes registros en sus tablas [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y [Property.](property-table.md) Todos los productos relacionados del grupo tienen el mismo UpgradeCode, pero el instalador no instala este paquete de actualización si ya hay una versión posterior a la 3.0 instalada en el equipo. En este caso, el instalador presenta un mensaje de error y se produce un error en la instalación. El paquete de actualización de la versión 3.0 se instala en las versiones 1.0 y 2.0.

    [Actualizar tabla](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | Lenguaje | Atributos                                | Remove | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

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

    

     

 

 



