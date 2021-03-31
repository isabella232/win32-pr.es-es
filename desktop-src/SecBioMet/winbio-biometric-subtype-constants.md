---
title: Constantes de WINBIO_BIOMETRIC_SUBTYPE (Winbio \_ Types. h)
description: Proporcionar información sobre una medida biométrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996614"
---
# <a name="winbio_biometric_subtype-constants"></a>WINBIO \_ constantes de \_ subtipo de biométrico

**WINBIO \_ Las constantes de \_ SUBtipo biométrico** se usan en el plataforma de biometría de Windows para proporcionar información adicional sobre una medida biométrica. Se pueden usar las siguientes constantes cuando no se requiere ningún subtipo o cuando se requiere un subtipo.



| Constante o valor                                                                                                                                                                                                                                                            | Descripción                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ \_No \_ información de subtipos**</dt> <dt>0x00</dt> </dl> | No hay información de subtipos.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ Subtipo \_**</dt> de <dt>0xFF</dt> </dl>                                   | Cualquier subtipo.<br/>            |



## <a name="remarks"></a>Observaciones

Para buscar los subtipos biométricos disponibles para un tipo de biométrico determinado, use la tabla siguiente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> valor</th>
<th>Temas para buscar valores de <strong>WINBIO_BIOMETRIC_SUBTYPE</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>Constantes de WINBIO_ANSI_385_FACE</strong></a>
<blockquote>
[!Note]<br />
Estos valores solo se aplican a Windows 10 y versiones posteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Uno de los temas siguientes:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>Constantes de WINBIO_ANSI_381_FORMAT</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMG</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMG_ACQ</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMP_TYPE</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>Constantes de WINBIO_ANSI_381_PIXELS</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Constantes de huella digital WINBIO_ANSI_381_POS</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Constantes de WINBIO_ANSI_381_POS_Palm</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>Constantes de WINBIO_IRIS</strong></a>
<blockquote>
[!Note]<br />
Estos valores solo se aplican a Windows 10 y versiones posteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Constantes de WINBIO_VOICE</strong></a>
<blockquote>
[!Note]<br />
Estos valores solo se aplican a Windows 10 y versiones posteriores.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Para obtener más información, consulte [constantes de aplicación cliente](client-application-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



 

 





