---
title: WINBIO_SETTING_SOURCE constantes (Winbio \_ types.h)
description: Determine si el Windows Biometric Framework está habilitado actualmente.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271287"
---
# <a name="winbio_setting_source-constants"></a>CONSTANTES DE \_ ORIGEN DE CONFIGURACIÓN DE WINBIO \_

La función [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) usa las siguientes constantes para determinar si el Windows Biometric Framework está habilitado actualmente. Las constantes especifican dónde se originó la configuración.



| Constante                                                                                                                                                                                                        | Descripción                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**EL ORIGEN DE CONFIGURACIÓN DE WINBIO \_ \_ NO ES \_ VÁLIDO**</dt> </dl> | La configuración no es válida.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**CONFIGURACIÓN PREDETERMINADA \_ DEL \_ ORIGEN DE \_ WINBIO**</dt> </dl> | La configuración se originó en la directiva integrada.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**CONFIGURACIÓN DE \_ LA DIRECTIVA DE ORIGEN DE \_ \_ WINBIO**</dt> </dl>    | La configuración se originó en el registro de equipo local.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**CONFIGURACIÓN LOCAL \_ DE \_ ORIGEN DE \_ WINBIO**</dt> </dl>       | La configuración la creó directiva de grupo<br/>                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





