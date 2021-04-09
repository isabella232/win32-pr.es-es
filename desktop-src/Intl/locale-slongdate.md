---
description: configuración regional \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154532"
---
# <a name="locale_slongdate"></a>configuración regional \_ SLONGDATE

Cadena de formato de fecha larga para la configuración regional. El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación. La cadena puede constar de una combinación de [imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md) y cualquier cadena de caracteres entre comillas simples. Los caracteres entre comillas simples permanecen como se especificó. Por ejemplo, la fecha larga española (España) es "dddd, DD ' de ' MMMM ' de ' YYYY". Las configuraciones regionales pueden definir varios formatos de fecha larga.

Para obtener todos los formatos de fecha larga de una configuración regional, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

 

 



