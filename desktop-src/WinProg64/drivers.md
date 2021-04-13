---
title: Controladores (Guía de programación para Windows de 64 bits)
description: La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una única base de código fuente para las aplicaciones de 32 bits y 64 bits. En gran medida, esto también se aplica a los controladores de Windows de 32 y 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- Controladores de 64 bits programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359640"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Controladores (Guía de programación para Windows de 64 bits)

La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una única base de código fuente para las aplicaciones de 32 bits y 64 bits. En gran medida, esto también se aplica a los controladores de Windows de 32 y 64 bits.

Sin embargo, los controladores de 32 bits no se pueden ejecutar en Windows de 64 bits y deben migrarse. En el caso de las aplicaciones de modo de usuario, Windows de 64 bits incluye WOW64, que permite que las aplicaciones Windows de 32 bits se ejecuten (con cierta pérdida de rendimiento) en sistemas que ejecutan Windows de 64 bits. No existe ninguna capa de traducción equivalente para los controladores.

Para obtener información sobre cómo migrar controladores a Windows de 64 bits, consulte [problemas de 64](https://msdn.microsoft.com/library/aa489627.aspx) bits en el kit de controladores de Windows (WDK).

 

 




