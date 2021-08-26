---
description: La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Acción InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996595"
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



 

## <a name="remarks"></a>Comentarios

La acción InstallAdminPackage también actualiza la información de resumen de la base de datos y quita los archivos archivadores ubicados en secuencias después de copiar la base de datos.

 

 



