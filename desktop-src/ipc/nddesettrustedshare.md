---
description: Concede el estado de confianza de recurso compartido DDE especificado en el contexto de usuarios actual.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Función NDdeSetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539963"
---
# <a name="nddesettrustedshare-function"></a>NDdeSetTrustedShare función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Concede el estado de confianza del recurso compartido DDE especificado en el contexto del usuario actual.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor cuyo DSDM se va a modificar.

</dd> <dt>

*lpszShareName* \[ de\]
</dt> <dd>

Nombre del recurso compartido al que se va a conceder el estado de confianza. Este parámetro no puede ser **null**.

</dd> <dt>

*dwTrustOptions* \[ de\]
</dt> <dd>

Opciones que afectan al estado de confianza del recurso compartido DDE. Este parámetro puede ser uno de los valores siguientes.



| Opción                                                                                                                                                                                                                                                      | Significado                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt> </dl>             | Máscara usada para obtener el valor que se usa para invalidar el estado de presentación del recurso compartido DDE, si \_ \_ se establece NDDE Trust cmd \_ Show.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ CONFIAR en \_ cmd \_ Mostrar**</dt> <dt>0x10000000L</dt> </dl>          | Invalide el estado de la presentación especificado en el DSDM del recurso compartido DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ \_Recurso compartido \_ de confianza del**</dt> <dt>0x20000000L</dt> </dl>       | Quite el estado de confianza del recurso compartido.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L de inicio de \_ recurso \_ compartido de confianza**</dt> <dt></dt> </dl>    | Permita que un cliente se inicie en la aplicación si ya se está ejecutando en el contexto del usuario.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ \_ \_ Inicio del recurso compartido de confianza**</dt> <dt>0x80000000L</dt> </dl> | Permite que la aplicación se inicie en el contexto del usuario.<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

El recurso compartido DDE debe crearse primero con [**NDdeShareAdd**](nddeshareadd.md).

Si se llama a **NDdeSetTrustedShare** con *dwTrustOptions* establecido en cero, el recurso compartido de confianza pierde su estado de confianza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeSetTrustedShareW** (Unicode) y **NDdeSetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




