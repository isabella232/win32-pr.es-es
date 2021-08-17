---
description: Un ensamblado Win32 se puede instalar como un ensamblado privado y estar disponible exclusivamente para su uso por una aplicación. Los ensamblados privados deben instalarse mediante un paquete Windows Installer que se usa para instalar o actualizar una aplicación.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Ensamblados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cc9bd9c9f4c5230dcb24ed7059f6817d4c5f3c7cfdeb4b7cfd25d95ca2a3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327854"
---
# <a name="private-assemblies"></a>Ensamblados privados

Un ensamblado Win32 se puede instalar como un ensamblado privado y estar disponible exclusivamente para su uso por una aplicación. Los ensamblados privados deben instalarse mediante un paquete Windows Installer que se usa para instalar o actualizar una aplicación.

En Windows XP, los ensamblados privados se instalan como [ensamblados en paralelo](side-by-side-assemblies.md). El Windows instala ensamblados privados en paralelo en una carpeta privada de la aplicación. Normalmente, la carpeta que contiene el archivo ejecutable de aplicaciones. La dependencia de la aplicación en el ensamblado privado se especifica en un archivo de manifiesto de aplicación. Para obtener más información, [vea Aplicaciones aisladas y ensamblados en paralelo.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

En sistemas operativos anteriores a Windows XP, se instala una copia del ensamblado privado y un archivo .local en una carpeta privada para el uso exclusivo de la aplicación. Una versión del ensamblado también se registra globalmente en el sistema y está disponible para cualquier aplicación que se enlaza a él. La versión global del ensamblado puede ser la versión instalada con la aplicación o una versión anterior. La versión global viene determinada por las mismas reglas que usan [los componentes aislados.](isolated-components.md)

Tenga en cuenta que Windows Installer no puede instalar un ensamblado privado en una ubicación que tenga una ruta de acceso que contenga más de 234 caracteres, incluido el carácter nulo de terminación.

 

 
