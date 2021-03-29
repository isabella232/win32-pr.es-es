---
description: El motor de configuración de seguridad llama a la función SceSvcAttachmentConfig cuando el sistema está configurado.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Función de devolución de llamada SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809302"
---
# <a name="scesvcattachmentconfig-callback-function"></a>Función de devolución de llamada SceSvcAttachmentConfig

El motor de configuración de seguridad llama a la función **SceSvcAttachmentConfig** cuando el sistema está configurado.

## <a name="syntax"></a>Sintaxis


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSceCbInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ información de devolución de llamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene el identificador de base de datos y las funciones de devolución de llamada para consultar, establecer y liberar información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve SCESTATUS \_ Success. En caso contrario, devuelve un código de error. Para obtener más información sobre los códigos de error de configuración de seguridad, vea [valores devueltos de datos adjuntos](management-return-values.md).

## <a name="remarks"></a>Observaciones

Al implementar esta función, use la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar la información de configuración. A continuación, configure el servicio con la información devuelta.

Esta función debe hacer lo siguiente:

-   Consulte la información de configuración del conjunto de herramientas de configuración de seguridad con la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).
-   Configure el servicio con la información de configuración.

Para obtener más información, consulte [implementación de SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de devolución de llamada de SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




