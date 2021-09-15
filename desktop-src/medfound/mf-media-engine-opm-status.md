---
description: Define el estado de Output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474182"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>MF \_ MEDIA \_ ENGINE \_ OPM STATUS \_ (enumeración)

Define el estado de [Output Protection Manager](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ NOT \_ REQUESTED**
</dt> <dd>

Estado predeterminado. Se usa para devolver el estado correcto cuando el contenido está desprotegido.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ ESTABLISHED**
</dt> <dd>

OPM establecido correctamente.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MÁQUINA \_ VIRTUAL CON ERROR DE MF MEDIA ENGINE \_ \_ OPM \_ \_**
</dt> <dd>

Error de OPM porque se ejecuta en una máquina virtual (VM).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED \_ BDA**
</dt> <dd>

Error de OPM porque no hay ningún controlador de gráficos y el sistema usa el adaptador de pantalla básico (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED \_ UNSIGNED \_ DRIVER**
</dt> <dd>

Error de OPM porque el controlador de gráficos no está firmado por PE y vuelve a WARP.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED**
</dt> <dd>

Error de OPM por otros motivos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation enumeraciones](media-foundation-enumerations.md)
</dt> </dl>

 

 




