---
description: WIA proporciona una capa de compatibilidad de TWAIN que permite a las aplicaciones compatibles con TWAIN comunicarse con dispositivos de adquisición de imágenes de Windows (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidad con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696507"
---
# <a name="twain-compatibility"></a>Compatibilidad con TWAIN

WIA proporciona una capa de compatibilidad de TWAIN que permite a las aplicaciones compatibles con TWAIN comunicarse con dispositivos de adquisición de imágenes de Windows (WIA). Las aplicaciones que reconocen TWAIN no tienen acceso total a la funcionalidad de WIA. Por ejemplo, una aplicación no puede suprimir la interfaz de usuario mediante el nivel de compatibilidad TWAIN.

Los dispositivos WIA aparecen dos veces en una aplicación que es consciente de WIA y TWAIN: una vez a través de una comunicación WIA normal y otra a través de la capa de compatibilidad TWAIN. Para evitar que se muestren dos veces un dispositivo WIA, una aplicación que tenga en cuenta WIA y TWAIN debe filtrar los dispositivos WIA que provienen del nivel de compatibilidad TWAIN. Todos los dispositivos WIA que atraviesan el nivel de compatibilidad TWAIN tienen "WIA-" como prefijo, por lo que es fácil filtrarlos.

 

 



