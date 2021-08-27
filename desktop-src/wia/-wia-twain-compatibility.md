---
description: WIA proporciona una capa de compatibilidad de TWAIN que permite que las aplicaciones compatibles con TWAIN se comuniquen con Windows de adquisición de imágenes (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidad con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056985"
---
# <a name="twain-compatibility"></a>Compatibilidad con TWAIN

WIA proporciona una capa de compatibilidad de TWAIN que permite que las aplicaciones compatibles con TWAIN se comuniquen con Windows de adquisición de imágenes (WIA). Las aplicaciones compatibles con TWAIN no tienen acceso completo a la funcionalidad de WIA. Por ejemplo, una aplicación no puede suprimir la interfaz de usuario mediante la capa de compatibilidad TWAIN.

Los dispositivos WIA aparecen dos veces en una aplicación que es consciente de WIA y TWAIN: una vez a través de la comunicación WIA normal y otra a través de la capa de compatibilidad de TWAIN. Para evitar enumerar dos veces un dispositivo WIA, una aplicación que sea consciente de WIA y TWAIN debe filtrar los dispositivos WIA que se incluyen a través de la capa de compatibilidad de TWAIN. Todos los dispositivos WIA que pasan a través de la capa de compatibilidad TWAIN tienen "WIA-" como prefijo, por lo que es fácil filtrarlos.

 

 



