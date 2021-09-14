---
description: En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: A qué versión de biblioteca se va a hacer referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362894"
---
# <a name="which-library-version-to-reference"></a>A qué versión de biblioteca se va a hacer referencia

En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versiones de la biblioteca de TABLET PC

Los archivos binarios de la biblioteca de Tablet PC (Microsoft.Ink.dll) se han actualizado en Windows Vista. Estos archivos binarios se conocen como "versión 6.0" para coexistir con la versión de Windows en la que se van a publicar.

La versión más reciente de los archivos binarios compatibles con Windows XP se conoce como "versión 1.7".

El SDK Windows se puede instalar en máquinas Vista y XP, y el SDK de Windows incluye ambas versiones de Microsoft.Ink.dll.

Estos se instalan en:

1. %programfiles% \\ Ensamblados de referencia \\ de Microsoft Tablet PC \\ \\ v1.7 \\Microsoft.Ink.dll

2. %programfiles% \\ Ensamblados de referencia \\ de Microsoft Tablet PC \\ \\ v6.0 \\Microsoft.Ink.dll

Los archivos binarios de la versión 6.0 solo son compatibles con Windows Vista y las aplicaciones escritas en ellos solo se deben ejecutar en Windows Vista.

Una aplicación escrita con los archivos binarios de la versión 1.7 debe ejecutarse sin modificaciones cuando se instala Windows Vista.

 

 



