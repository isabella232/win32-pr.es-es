---
description: Un usuario puede comprobar el estado de la interfaz teredo desde el símbolo del sistema escribiendo netsh interface teredo show state y examinando la salida.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Infraestructura del mismo nivel y Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794242"
---
# <a name="the-peer-infrastructure-and-teredo"></a>Infraestructura del mismo nivel y Teredo

Un usuario puede comprobar el estado de la interfaz [teredo](https://msdn.microsoft.com/library/ms819742.aspx) desde el símbolo del sistema escribiendo **netsh interface teredo show state** y examinando la salida. Si el estado es "sin conexión", Teredo no está activo, lo que impide que el usuario se conecte a otros usuarios a través de sus direcciones de Teredo. Es posible que Teredo esté sin conexión porque el firewall está deshabilitado o no admite [IPv6.](/previous-versions/windows/embedded/ms898970(v=msdn.10))

 

 
