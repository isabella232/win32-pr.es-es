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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259468"
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

*pSceCbInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene un identificador de base de datos opaco y punteros de función de devolución de llamada para consultar, establecer y liberar información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve SCESTATUS \_ SUCCESS. De lo contrario, devuelve un código de error. Para obtener más información sobre los códigos de error de configuración de seguridad, vea [Valores devueltos de datos adjuntos.](management-return-values.md)

## <a name="remarks"></a>Observaciones

La **función SceSvcAttachmentAnalyze** debe hacer lo siguiente:

-   Consulte directamente la información de configuración del servicio.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar información de la base de datos de seguridad.
-   Calcule las diferencias entre la información en función del tipo y la sintaxis.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para actualizar la base de datos de seguridad con la información del servicio recuperada que es diferente.

Para obtener más información, [vea Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Implementación de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**INFORMACIÓN DE DEVOLUCIÓN DE LLAMADA DE SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




