---
title: Seguimiento de los intervalos modificados de un archivo
description: Seguimiento de los intervalos modificados de un archivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705051"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Seguimiento de los intervalos modificados de un archivo

## <a name="platforms"></a>Plataformas

**Clientes-** Windows 8.1 (todas las SKU)  
**Servidores:** Windows Server 2012 R2  

## <a name="description"></a>Descripción

El equipo del sistema de archivos NT (NTFS) ha agregado una nueva característica a Windows. El diario USN generará un registro de número de secuencia de actualización (USN) que contiene los intervalos modificados de un archivo al cerrarse. Se ha introducido un nuevo tipo de registro, el \_ registro USN \_ V4 para registrar estos intervalos modificados de un archivo.

La característica no está habilitada de forma predeterminada; los usuarios deben invocar un comando de control del sistema de archivos (FSCTL) para habilitarlo. Sin embargo, dado que otros componentes de Windows pueden activar el seguimiento de intervalos, los usuarios y los desarrolladores pueden percibir que la característica está siempre habilitada. Windows permitirá a los desarrolladores consultar el diario USN para averiguar si está habilitado el seguimiento de intervalo.

La documentación de MSDN se proporcionará en una fecha posterior para instruir a los desarrolladores sobre cómo acceder a \_ los registros de registro de USN \_ V4.

## <a name="manifestation"></a>Manifestación

Todas las aplicaciones existentes que usan el diario USN seguirán funcionando bien sin problemas de compatibilidad.

 

 




