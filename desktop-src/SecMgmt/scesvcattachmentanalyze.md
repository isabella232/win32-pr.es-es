---
description: El motor de configuración de seguridad llama a la función SceSvcAttachmentAnalyze cuando se analiza el sistema.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Función de devolución de llamada SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809307"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Función de devolución de llamada SceSvcAttachmentAnalyze

El motor de configuración de seguridad llama a la función **SceSvcAttachmentAnalyze** cuando se analiza el sistema.

## <a name="syntax"></a>Sintaxis


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSceCbInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ información de devolución de llamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene un identificador de base de datos opaco y punteros de función de devolución de llamada para consultar, establecer y liberar información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve SCESTATUS \_ Success. En caso contrario, devuelve un código de error. Para obtener más información sobre los códigos de error de configuración de seguridad, vea [valores devueltos de datos adjuntos](management-return-values.md).

## <a name="remarks"></a>Observaciones

La función **SceSvcAttachmentAnalyze** debe hacer lo siguiente:

-   Consulte directamente la información de configuración del servicio.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar información de la base de datos de seguridad.
-   Calcular las diferencias entre la información basada en el tipo y la sintaxis.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para actualizar la base de datos de seguridad con la información de servicio recuperada que sea diferente.

Para obtener más información, consulte [implementación de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Implementación de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**información de devolución de llamada de SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




