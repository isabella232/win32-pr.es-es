---
description: En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: La versión de la biblioteca a la que se hace referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696332"
---
# <a name="which-library-version-to-reference"></a>La versión de la biblioteca a la que se hace referencia

En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versiones de la biblioteca de Tablet PC

Los archivos binarios de la biblioteca de Tablet PC (Microsoft.Ink.dll) se han actualizado en Windows Vista. Estos archivos binarios se conocen como "versión 6,0" para incide con la versión de Windows en la que se publican.

La versión más reciente de los binarios que son compatibles con Windows XP se conoce como "versión 1,7".

El Windows SDK se puede instalar en las máquinas con vista y XP, y el Windows SDK incluye ambas versiones de Microsoft.Ink.dll.

Se instalan en:

1. % programfiles% \\ Reference assemblies \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll

2. % programfiles% de \\ ensamblados de referencia \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll

Los archivos binarios de la versión 6,0 solo son compatibles con Windows Vista y las aplicaciones escritas en ellos solo deben ejecutarse en Windows Vista.

Una aplicación escrita en los archivos binarios de la versión 1,7 debe ejecutarse sin modificaciones cuando se instala en Windows Vista.

 

 



