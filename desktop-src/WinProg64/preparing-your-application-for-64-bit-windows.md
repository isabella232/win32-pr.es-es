---
title: Preparar la aplicación para aplicaciones de 64 bits Windows
description: Hay varias características que facilitan el desarrollo de aplicaciones que se ejecutarán en aplicaciones de 32 y 64 bits Windows. La mayoría de ellos, como los nuevos tipos de datos, se describen en Getting Ready for 64-bit Windows (Prepararse para los tipos de datos de 64 Windows).
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Programación del kit de herramientas de 64 bits Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071625"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Preparar la aplicación para aplicaciones de 64 bits Windows

Hay varias características que facilitan el desarrollo de aplicaciones que se ejecutarán en aplicaciones de 32 y 64 bits Windows. La mayoría de ellos, como los nuevos tipos de datos, se describen en [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

El kit de herramientas de 64 bits que se incluye con el SDK de Windows incluye un compilador MIDL de 64 bits, Midl.exe, para generar códigos auxiliares nativos de 64 bits, así como códigos auxiliares de 32 bits. Use el **modificador /env win64** para generar solo código auxiliar de 64 bits. El valor predeterminado es generar código auxiliar dual que se ejecute en ambas plataformas.

Tenga en cuenta que MIDL de 64 bits solo admite los modos de optimización [**/Oicf**](/windows/desktop/Midl/-oi) y [**/Os.**](/windows/desktop/Midl/-os)

 

 