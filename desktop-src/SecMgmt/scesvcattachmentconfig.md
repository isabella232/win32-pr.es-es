---
description: El motor de configuración de seguridad llama a la función SceSvcAttachmentConfig cuando se configura el sistema.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259455"
---
# <a name="scesvcattachmentconfig-callback-function"></a>Función de devolución de llamada SceSvcAttachmentConfig

El motor de configuración de seguridad llama a la función **SceSvcAttachmentConfig** cuando se configura el sistema.

## <a name="syntax"></a>Sintaxis


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSceCbInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene el identificador de base de datos y las funciones de devolución de llamada para consultar, establecer y liberar información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve SCESTATUS \_ SUCCESS. De lo contrario, devuelve un código de error. Para obtener más información sobre los códigos de error de configuración de seguridad, vea [Valores devueltos de datos adjuntos](management-return-values.md).

## <a name="remarks"></a>Observaciones

Al implementar esta función, use la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar información de configuración. A continuación, configure el servicio con la información devuelta.

Esta función debe hacer lo siguiente:

-   Consulte la información de configuración del conjunto de herramientas configuración de seguridad mediante la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).
-   Configure el servicio mediante la información de configuración.

Para obtener más información, [vea Implementing SceSvcAttachmentConfig (Implementación de SceSvcAttachmentConfig).](implementing-scesvcattachmentconfig.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INFORMACIÓN DE DEVOLUCIÓN DE LLAMADA SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




