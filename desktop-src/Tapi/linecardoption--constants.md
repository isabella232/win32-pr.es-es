---
description: Las \_ constantes LINECARDOPTION definen los valores que se usan en el miembro dwOptions de la estructura LINECARDENTRY devuelta como parte de la estructura LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes de LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681233"
---
# <a name="linecardoption_-constants"></a>Constantes de LINECARDOPTION \_

Las **\_ constantes LINECARDOPTION** definen los valores que se usan en el miembro **DwOptions** de la estructura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps). Las **\_ constantes de LINECARDOPTION** t tienen los siguientes valores:

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ oculto**
</dt> <dd> <dl> <dt>



El usuario ha ocultado esta tarjeta de llamada. No se muestra en la aplicación auxiliar de marcado en la lista principal de tarjetas de llamada disponibles, pero se mostrará en la lista de tarjetas de las que se pueden copiar reglas de marcado.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ PREdefinido**
</dt> <dd> <dl> <dt>



Esta tarjeta de llamada es una de las definiciones de tarjeta de llamada predefinidas incluidas con telefonía por Microsoft. No se puede quitar completamente mediante la aplicación auxiliar de marcado; Si el usuario intenta quitarlo, se quedará oculto. Por lo tanto, sigue siendo accesible para copiar reglas de marcado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

No extensible. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




