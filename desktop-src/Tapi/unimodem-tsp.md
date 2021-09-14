---
description: El TSP (Unimdm.tsp) unimodem o controlador de módem universal proporciona acceso a casi todos los módems estándar.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168853"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

El TSP (Unimdm.tsp) unimodem o controlador de módem universal proporciona acceso a casi todos los módems estándar. Admite módems de voz que permiten el streaming semidúplex. Son compatibles con el MSP de Wave y el control de flujo es posible. (Tenga en cuenta que Unimodem en Windows NT 4.0 o versiones anteriores no admite módems de voz, por lo que no es posible el control de flujo directo).

Este TSP admite un valor [**de tipo de**](./lineaddresstype--constants.md) dirección LINEADDRESSTYPE \_ PHONENUMBER. Si el programador quiere usar las reglas de marcado, la interfaz [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) de TAPI 3 o la función TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) deben usarse para obtener una cadena que se puede marcar a partir de un número de teléfono en formato canónico.

Unimodem TSP se instala con los sistemas operativos Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Edition, Windows 98 y Windows 95.

 

 
