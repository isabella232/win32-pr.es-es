---
title: Copias de seguridad y restauración de Windows 7 en desuso
description: Copias de seguridad y restauración de Windows 7 en desuso
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105676515"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Copias de seguridad y restauración de Windows 7 en desuso

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


## <a name="description"></a>Descripción

Aunque no hay ningún cambio de comportamiento en la copia de seguridad y la restauración, esta función está en desuso y no se actualizará. Rara vez se usaba y su funcionalidad se ha reemplazado por la nueva característica historial de archivos. Se incluirá en Windows 8 y entusiastas que se hayan actualizado de Windows 7 a Windows 8 o que dependan de la copia de seguridad y la restauración, o bien que la copia de seguridad de la imagen de disco siga pudiendo usarla. Sin embargo, se han quitado todos los puntos de acceso a la copia de seguridad y restauración, con la excepción del panel de control. Se ha cambiado el nombre del applet del panel de control usado por copias de seguridad y restauración a recuperación de archivos de Windows 7.

Los OEM que establecieron la clave del registro para deshabilitar la notificación de copias de seguridad en sus imágenes ya no tendrán que hacerlo.

No se recomienda usar ambas características al mismo tiempo. El historial de archivos comprueba si existe una programación de copia de seguridad y está activa y, si encuentra alguna, no permitirá que los usuarios la activen. En este caso, los usuarios que deseen usar el historial de archivos tendrán que eliminar la programación de copias de seguridad de Windows.

## <a name="manifestation"></a>Manifestación

Los flujos de trabajo se pueden interrumpir y es necesario actualizar la documentación que hace referencia al método anterior para tener acceso a la característica copia de seguridad y restauración de Windows para reflejar estos cambios.

## <a name="mitigation"></a>Mitigación

Las aplicaciones que pueden desencadenar copias de seguridad y restauración se deben volver a escribir para comprobar si el historial de archivos está activado y permitir que los usuarios elijan su método preferido.

 

 




