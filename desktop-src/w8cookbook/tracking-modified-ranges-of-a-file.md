---
title: Seguimiento de los intervalos modificados de un archivo
description: Seguimiento de los intervalos modificados de un archivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6998d2706cd4d8bdb4e94b95fd0e617dbbf4e3a1b288d33dbcebe5528d544c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852032"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Seguimiento de los intervalos modificados de un archivo

## <a name="platforms"></a>Plataformas

**Clientes: Windows 8.1** (todas las SKU)  
**Servidores:** Windows Server 2012 R2  

## <a name="description"></a>Descripción

El equipo del sistema de archivos NT (NTFS) ha agregado una nueva característica a Windows. UsN Journal mostrará un registro de número de secuencia de actualización (USN) que contiene intervalos modificados para un archivo al cerrarse. Se ha introducido un nuevo tipo de registro, USN RECORD V4, para registrar \_ \_ estos intervalos modificados de un archivo.

La característica no está habilitada de forma predeterminada; Los usuarios deben invocar un comando de control del sistema de archivos (FSCTL) para habilitarlo. Sin embargo, dado que otros Windows pueden activar el seguimiento de intervalos, los usuarios y desarrolladores pueden percibir que la característica siempre está habilitada. Windows permitirá a los desarrolladores consultar el diario de USN para averiguar si está habilitado el seguimiento de intervalos.

La documentación de MSDN se proporciona más adelante para indicar a los desarrolladores cómo acceder a los registros DE USN \_ RECORD \_ V4.

## <a name="manifestation"></a>Manifestación

Todas las aplicaciones existentes que usan USN Journal seguirán funcionando bien sin problemas de compatibilidad.

 

 




