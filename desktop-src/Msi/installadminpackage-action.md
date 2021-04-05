---
description: La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Acción InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001710"
---
# <a name="installadminpackage-action"></a>Acción InstallAdminPackage

La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad [**targetDir**](targetdir.md) .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nombre de los archivos de instalación.                                     |
| \[6\] | Tamaño de la base de datos.                                          |
| \[9\] | Identificador de instalación administrativa: directorio de puntos. |



 

## <a name="remarks"></a>Observaciones

La acción InstallAdminPackage también actualiza la información de Resumen de la base de datos y quita los archivos. cab que se encuentran en los flujos una vez copiada la base de datos.

 

 



