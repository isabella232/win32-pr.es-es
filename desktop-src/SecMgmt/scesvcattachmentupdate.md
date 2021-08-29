---
description: Los complementos de configuración de seguridad llaman a la función SceSvcAttachmentUpdate para pasar los cambios de configuración a la base de datos de seguridad.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Función de devolución de llamada SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b04d8a144373ae493a956e2166ea6dab34d844c71504f303766e8de7915b9a70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004873"
---
# <a name="scesvcattachmentupdate-callback-function"></a>Función de devolución de llamada SceSvcAttachmentUpdate

Los complementos de configuración de seguridad llaman a la función **SceSvcAttachmentUpdate** para pasar los cambios de configuración a la base de datos de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSceCbInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene el identificador de devolución de llamada y los punteros de función a SCE.

</dd> <dt>

*ServiceInfo* \[ En\]
</dt> <dd>

Información de configuración actualizada. La estructura de datos utilizada para esta información es [**SCESVC \_ CONFIGURATION \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve SCESTATUS \_ SUCCESS. De lo contrario, devuelve un código de error. Para obtener más información sobre los códigos de error de configuración de seguridad, vea [Valores devueltos de datos adjuntos.](management-return-values.md)

## <a name="remarks"></a>Comentarios

La **función SceSvcAttachmentUpdate** debe hacer lo siguiente:

-   Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar la información de configuración base actual de la base de datos de seguridad.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar el último conjunto de diferencias (información de análisis) de la base de datos de seguridad.
-   Use la información de servicio proporcionada (consulte *ServiceInfo*) para calcular la nueva configuración base.
-   Use la información de servicio proporcionada (consulte *ServiceInfo*) y el análisis para calcular la nueva información de diferencia.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para establecer la nueva configuración base en la base de datos de seguridad.
-   Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para establecer la nueva información de análisis en la base de datos de seguridad.

Para obtener más información, [vea Implementing SceSvcAttachmentUpdate (Implementación de SceSvcAttachmentUpdate).](implementing-scesvcattachmentupdate.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE DEVOLUCIÓN DE LLAMADA DE SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**INFORMACIÓN DE CONFIGURACIÓN DE SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




