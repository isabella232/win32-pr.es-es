---
description: La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Acción InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171810"
---
# <a name="installadminpackage-action"></a>Acción InstallAdminPackage

La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la [**propiedad TARGETDIR.**](targetdir.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nombre de los archivos de instalación.                                     |
| \[6\] | Tamaño de la base de datos.                                          |
| \[9\] | Identificador del directorio de punto de instalación administrativa. |



 

## <a name="remarks"></a>Observaciones

La acción InstallAdminPackage también actualiza la información de resumen de la base de datos y quita los archivos archivadores ubicados en secuencias después de copiar la base de datos.

 

 



