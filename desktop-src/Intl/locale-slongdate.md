---
description: LOCALE \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e47409d99d4db9afa2e684d3be8ae2f874200d56d748868eaa0fa1953452d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106065"
---
# <a name="locale_slongdate"></a>LOCALE \_ SLONGDATE

Cadena de formato de fecha larga para la configuración regional. El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación. La cadena puede constar de una combinación de imágenes de formato [de día, mes, año y era](day--month--year--and-era-format-pictures.md) y cualquier cadena de caracteres entre comillas simples. Los caracteres entre comillas simples permanecen según lo especificado. Por ejemplo, la fecha larga de español (España) es "dddd, dd" de 'MMMM' de 'yyyy'. Las configuraciones regionales pueden definir varios formatos de fecha larga.

Para obtener todos los formatos de fecha larga de una configuración regional, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

 

 



