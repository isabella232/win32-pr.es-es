---
description: El Unimodem, o controlador de módem universal, TSP (Unimdm. TSP) proporciona acceso a casi todos los módems estándar.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP de Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688318"
---
# <a name="unimodem-tsp"></a>TSP de Unimodem

El Unimodem, o controlador de módem universal, TSP (Unimdm. TSP) proporciona acceso a casi todos los módems estándar. Admite módems de voz que permiten el streaming dúplex medio. Son compatibles con Wave MSP y el control de flujo es posible. (Tenga en cuenta que Unimodem en Windows NT 4,0 o versiones anteriores no es compatible con los módems de voz, por lo que no es posible el control de flujo directo).

Este TSP admite un valor de [**tipo de dirección**](./lineaddresstype--constants.md) de LINEADDRESSTYPE \_ PHONENUMBER. Si el programador desea usar las reglas de marcado, la interfaz [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) de TAPI 3 o la función [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) de TAPI 2 deben usarse para obtener una cadena de marcado desde un número de teléfono en formato canónico.

El TSP de Unimodem se instala con los sistemas operativos Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 y Windows 95.

 

 
