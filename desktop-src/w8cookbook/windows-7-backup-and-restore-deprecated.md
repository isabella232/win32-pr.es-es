---
title: Windows 7 Copia de seguridad y restauración en desuso
description: Windows 7 Copia de seguridad y restauración en desuso
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211234"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7 Copia de seguridad y restauración en desuso

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


## <a name="description"></a>Descripción

Aunque no hay ningún cambio de comportamiento en la copia de seguridad y restauración, esta función está en desuso y no se actualizará. Rara vez se usó y su funcionalidad se ha reemplazado por la nueva Historial de archivos característica. Se enviará en Windows 8 y los aficionados que actualizaron de Windows 7 a Windows 8 o dependen de la copia de seguridad y restauración o de la copia de seguridad de imágenes de disco seguirán siendo capaces de usarla. Sin embargo, se han quitado todos los puntos de acceso a Copia de seguridad y restauración, a excepción del Panel de control de acceso. El Panel de control applet usado por Copia de seguridad y restauración ha cambiado de nombre a Windows 7 File Recovery.

Los OEM que estaban estableciendo la clave del Registro para deshabilitar la notificación de copia de seguridad en sus imágenes ya no tendrán que hacerlo.

No se recomienda usar ambas características al mismo tiempo. Historial de archivos comprueba si la programación de copia de seguridad existe y está activa y, si encuentra una, no permitirá que los usuarios la activen. En este caso, los usuarios que quieran usar Historial de archivos tendrán que eliminar la Copias de seguridad de Windows programación.

## <a name="manifestation"></a>Manifestación

Los flujos de trabajo se pueden interrumpir y la documentación que hace referencia al método anterior para acceder a la característica Copias de seguridad de Windows y restauración deberá actualizarse para reflejar estos cambios.

## <a name="mitigation"></a>Mitigación

Las aplicaciones que podrían desencadenar la copia de seguridad y restauración deben reescribirse para comprobar si Historial de archivos está activado y permitir que los usuarios elijan su método preferido.

 

 




