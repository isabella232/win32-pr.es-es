---
description: Las \_ constantes LINELOCATIONOPTION definen los valores que se usan en el miembro dwOptions de la estructura LINELOCATIONENTRY devuelta como parte de la estructura LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes de LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680771"
---
# <a name="linelocationoption_-constants"></a>Constantes de LINELOCATIONOPTION \_

Las **constantes \_ LINELOCATIONOPTION** definen los valores que se usan en el miembro **DwOptions** de la estructura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



El modo de marcado predeterminado en esta ubicación es el marcado por pulsos. Si se establece este bit, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) insertará un modificador de marcado "P" al principio de la cadena de marcado devuelta cuando se seleccione esta ubicación. Si no se establece este bit, **lineTranslateAddress** insertará un modificador de marcado "T" al principio de la cadena de marcado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

No extensible. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




