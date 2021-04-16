---
description: Define el estado del administrador de protección de salida (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Enumeración MF_MEDIA_ENGINE_OPM_STATUS
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
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678627"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>\_ \_ \_ Enumeración de estado de OPM del motor multimedia MF \_

Define el estado del [Administrador de protección de salida](output-protection-manager.md) (OPM).

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

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_no se \_ \_ \_ \_ solicitó el OPM del motor de multimedia MF**
</dt> <dd>

Estado predeterminado. Se usa para devolver el estado correcto cuando el contenido no está protegido.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**se \_ \_ estableció el \_ OPM del motor de multimedia MF \_**
</dt> <dd>

OPM se estableció correctamente.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_error de \_ \_ \_ \_ máquina virtual de OPM del motor multimedia MF**
</dt> <dd>

Error de OPM porque se está ejecutando en una máquina virtual (VM).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**\_ \_ \_ \_ se produjo un error de OPM \_ BDA del motor multimedia MF**
</dt> <dd>

No se pudo usar OPM porque no hay ningún controlador de gráficos y el sistema usa el adaptador de pantalla básico (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ no se pudo iniciar el \_ controlador no firmado de OPM del motor \_ de multimedia MF**
</dt> <dd>

No se pudo ejecutar OPM porque el controlador de gráficos no está firmado por PE, revirtiendo a WARP.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_error de \_ OPM del motor multimedia \_ MF \_**
</dt> <dd>

No se pudo ejecutar OPM por otras razones.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




