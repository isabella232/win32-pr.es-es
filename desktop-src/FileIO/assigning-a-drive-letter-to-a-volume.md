---
description: 'Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función SetVolumeMountPoint, siempre que no haya ningún volumen ya asignado a esa letra de unidad).'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Asignación de una letra de unidad a un volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687287"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Asignación de una letra de unidad a un volumen

Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , siempre que no haya ningún volumen ya asignado a esa letra de unidad). Si el volumen local ya tiene una letra de unidad. a continuación, se producirá un error en [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) . Para controlar esto, elimine primero la letra de unidad mediante la función [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) . Para ver un ejemplo de código, consulte [edición de asignaciones de letra de unidad](editing-drive-letter-assignments.md).

El sistema admite como máximo una letra de unidad por volumen. Por lo tanto, no puede tener C: \\ y F: \\ representar el mismo volumen.

> [!Caution]
>
> La eliminación de una letra de unidad existente y la asignación de una nueva puede romper las rutas existentes, como las de los accesos directos del escritorio. También puede interrumpir la ruta de acceso al programa que realiza la letra de la unidad. Con la administración de la memoria virtual de Windows, esto puede interrumpir la aplicación, lo que deja el sistema en un estado inestable y posiblemente inutilizable. Es responsabilidad del diseñador de programas evitar tales posibles catástrofes.

 

 

 



