---
description: 'Puede asignar una letra de unidad (por ejemplo, X: a un volumen local mediante la función SetVolumeMountPoint, siempre que no haya ningún volumen asignado a esa letra \) de unidad).'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Asignar una letra de unidad a un volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766234"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Asignar una letra de unidad a un volumen

Puede asignar una letra de unidad (por ejemplo, X: a un volumen local mediante la función \) [**SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) siempre que no haya ningún volumen asignado a esa letra de unidad). Si el volumen local ya tiene una letra de unidad. a [**continuación, Se producirá un error en SetVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) Para controlar esto, elimine primero la letra de unidad mediante la [**función DeleteVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Para obtener código de ejemplo, vea [Edición de asignaciones de letra de unidad.](editing-drive-letter-assignments.md)

El sistema admite como máximo una letra de unidad por volumen. Por lo tanto, no puede hacer que C: \\ y F: \\ representen el mismo volumen.

> [!Caution]
>
> La eliminación de una letra de unidad existente y la asignación de una nueva puede interrumpir las rutas de acceso existentes, como las de los accesos directos de escritorio. También puede interrumpir la ruta de acceso al programa que realiza los cambios en la letra de unidad. Con Windows administración de memoria virtual, esto puede interrumpir la aplicación, lo que deja el sistema en un estado inestable y posiblemente inutilizable. Es responsabilidad del diseñador de programas evitar estas posibles catástrofes.

 

 

 



