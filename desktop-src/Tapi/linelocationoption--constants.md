---
description: Las constantes LINELOCATIONOPTION definen valores utilizados en el miembro dwOptions de la estructura LINELOCATIONENTRY devuelta como parte de la estructura \_ LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45de77a6d887b6fb0c5fa0e45e7005a621aa10ca44cc3218078eea74d00a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003053"
---
# <a name="linelocationoption_-constants"></a>LineLOCATIONOPTION \_ (constantes)

Las **constantes \_ LINELOCATIONOPTION** definen los valores utilizados en el **miembro dwOptions** de la estructura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



El modo de marcado predeterminado en esta ubicación es el de pulsación. Si se establece este bit, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) insertará un modificador de marcado "P" al principio de la cadena que se puede marcar devuelta cuando se selecciona esta ubicación. Si no se establece este bit, **lineTranslateAddress** insertará un modificador de marcado "T" al principio de la cadena que se puede marcar.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

No extensible. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




