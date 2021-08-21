---
description: Las constantes LINECARDOPTION definen valores utilizados en el miembro dwOptions de la estructura LINECARDENTRY devuelta como parte de la estructura \_ LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: LINECARDOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6155d9e8da6036642e5275f5554a25743e57d9bcf6403411a52d144fc7d99bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863833"
---
# <a name="linecardoption_-constants"></a>LINECARDOPTION \_ (Constantes)

Las **constantes \_ LINECARDOPTION** definen valores utilizados en el **miembro dwOptions** de la estructura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps). Las **constantes LINECARDOPTION \_** t tienen los siguientes valores:

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ HIDDEN**
</dt> <dd> <dl> <dt>



El usuario ha ocultado esta tarjeta de llamada. El asistente de marcado no lo muestra en la lista principal de tarjetas de llamada disponibles, pero se mostrará en la lista de tarjetas de las que se pueden copiar las reglas de marcado.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ PREDEFINIDO**
</dt> <dd> <dl> <dt>



Esta tarjeta de llamada es una de las definiciones predefinidas de tarjetas de llamada incluidas con Telefonía por Microsoft. No se puede quitar por completo mediante el asistente de marcado; Si el usuario intenta quitarlo, se convertirá en HIDDEN. Por lo tanto, sigue siendo accesible para copiar las reglas de marcado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

No extensible. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




