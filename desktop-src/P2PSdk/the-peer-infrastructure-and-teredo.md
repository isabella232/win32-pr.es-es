---
description: Un usuario puede comprobar el estado de la interfaz Teredo desde el símbolo del sistema escribiendo netsh interface Teredo show State y examinando la salida.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: La infraestructura del mismo nivel y Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545518"
---
# <a name="the-peer-infrastructure-and-teredo"></a>La infraestructura del mismo nivel y Teredo

Un usuario puede comprobar el estado de la interfaz [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) desde el símbolo del sistema escribiendo **netsh interface Teredo show State** y examinando la salida. Si el estado es "sin conexión", Teredo no está activo, lo que impide que el usuario se conecte a otros usuarios a través de sus direcciones Teredo. Es posible que Teredo esté sin conexión porque el Firewall está deshabilitado o no es compatible con [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).

 

 
