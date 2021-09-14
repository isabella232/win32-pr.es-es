---
title: WINBIO_BIOMETRIC_SUBTYPE constantes (Winbio \_ types.h)
description: Proporcione información sobre una medida biométrica.
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
ms.openlocfilehash: 07e6dc285e1a19fab8e0363391fbd81429e931cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160786"
---
# <a name="winbio_biometric_subtype-constants"></a>Constantes \_ DE \_ SUBTIPO BIOMÉTRICO DE WINBIO

**WINBIO \_ Las constantes \_ BIOMETRIC SUBTYPE** se usan en Windows marco biométrico para proporcionar información adicional sobre una medida biométrica. Las siguientes constantes se pueden usar cuando no se requiere ningún subtipo o cuando se requiere algún subtipo.



| Constante o valor                                                                                                                                                                                                                                                            | Descripción                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ SUBTIPO \_ SIN \_ INFORMACIÓN**</dt> <dt>0x00</dt> </dl> | No hay información de subtipo.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ SUBTIPO \_ CUALQUIER**</dt> <dt>0xFF</dt> </dl>                                   | Cualquier subtipo.<br/>            |



## <a name="remarks"></a>Observaciones

Para buscar los subtipos biométricos disponibles para un tipo biométrico determinado, use la tabla siguiente:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> valor</th>
<th>Temas para buscar <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> valores</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE constantes</strong></a>
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
<li><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT constantes</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG constantes</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ constantes</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE constantes</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS constantes</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS constantes de huella digital</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm constantes</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS constantes</strong></a>
<blockquote>
[!Note]<br />
Estos valores solo se aplican a Windows 10 y versiones posteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE constantes</strong></a>
<blockquote>
[!Note]<br />
Estos valores solo se aplican a Windows 10 y versiones posteriores.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Para obtener más información, vea [Constantes de aplicación cliente](client-application-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



 

 





