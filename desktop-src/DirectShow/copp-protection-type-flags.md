---
description: Las constantes siguientes se usan con el protocolo de protección de salida (COPP) certificado para los mecanismos de protección de salida específicos.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Marcas de tipo de protección COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671802"
---
# <a name="copp-protection-type-flags"></a>Marcas de tipo de protección COPP

Las constantes siguientes se usan con el protocolo de protección de salida (COPP) certificado para los mecanismos de protección de salida específicos.



| Constante o valor                                                                                                                                                                                                                                                                                                             | Descripción                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**COPP \_ ProtectionType \_**</dt> de <dt>0x80000000</dt> desconocido </dl>     | Mecanismo de protección desconocido.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**COPP \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt> </dl>                 | Sin mecanismos de protección.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**COPP \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth Digital Content Protection (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**COPP \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Protección de copia analógica (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**COPP \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Copiar sistema de administración de generación analógico (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**COPP \_ ProtectionType \_ Mask**</dt> <dt>0x80000007</dt> </dl>                 | Máscara de máscara para aislar marcas válidas.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**COPP \_ ProtectionType \_ reservado**</dt> <dt>0x7FFFFFF8</dt> </dl> | Reservado. Debe ser cero.<br/>                              |



## <a name="remarks"></a>Observaciones

Algunos métodos devuelven una única marca de este tipo de enumeración y algunos métodos devuelven una **o** varias de ellas.

Estas marcas se usan en las siguientes consultas y comandos de COPP.

-   Nivel de protección global
-   Nivel de protección local
-   Tipo de protección
-   Establecer el nivel de protección

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




