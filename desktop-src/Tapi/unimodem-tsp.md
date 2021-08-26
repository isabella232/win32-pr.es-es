---
description: Unimodem, o controlador de módem universal, TSP (Unimdm.tsp) proporciona acceso a casi todos los módems estándar.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4562ad7692c288a963db27b6859fa5c472d8ff80017e2726c277fbf9d24452be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011905"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

Unimodem, o controlador de módem universal, TSP (Unimdm.tsp) proporciona acceso a casi todos los módems estándar. Admite módems de voz que permiten el streaming semidúplex. Son compatibles con el MSP de Wave y el control de flujo es posible. (Tenga en cuenta que Unimodem en Windows NT 4.0 o versiones anteriores no admite módems de voz, por lo que no es posible el control de flujo directo).

Este TSP admite un [**valor de tipo de**](./lineaddresstype--constants.md) dirección de LINEADDRESSTYPE \_ PHONENUMBER. Si el programador quiere usar las reglas de marcado, la interfaz [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) de TAPI 3 o la función tapi 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) deben usarse para obtener una cadena que se puede marcar a partir de un número de teléfono en formato canónico.

Unimodem TSP se instala con los sistemas operativos Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 y Windows 95.

 

 
