---
title: Controladores (Guía de programación para aplicaciones de 64 Windows)
description: La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una base de código fuente única para sus aplicaciones de 32 y 64 bits. En gran medida, esto también se aplica a los controladores de 32 y 64 Windows bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- programación de controladores de 64 Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132858"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Controladores (Guía de programación para aplicaciones de 64 Windows)

La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una base de código fuente única para sus aplicaciones de 32 y 64 bits. En gran medida, esto también se aplica a los controladores de 32 y 64 Windows bits.

Sin embargo, los controladores de 32 bits no se pueden ejecutar en Windows de 64 bits y se deben porte. En el caso de las aplicaciones en modo de usuario, Windows de 64 bits incluye WOW64, que permite que las aplicaciones Windows de 32 bits se ejecuten (con cierta pérdida de rendimiento) en sistemas que ejecutan aplicaciones de 64 bits Windows. No existe ninguna capa de traducción equivalente para los controladores.

Para obtener información sobre la porción de controladores a Windows de 64 bits, vea Problemas de [64](https://msdn.microsoft.com/library/aa489627.aspx) bits en Windows Driver Kit (WDK).

 

 




