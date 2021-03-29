---
description: Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de usuarios del servidor de recursos compartidos de confianza.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Función NDdeGetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666245"
---
# <a name="nddegettrustedshare-function"></a>NDdeGetTrustedShare función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*lpszShareName* \[ de\]
</dt> <dd>

Nombre del recurso compartido cuyo estado de confianza se está consultando. Este parámetro no puede ser **null**.

</dd> <dt>

*lpdwTrustOptions* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe las opciones de confianza. Este parámetro no puede ser **null**. Están disponibles las siguientes opciones de confianza.



| Value                                                                                                                                                                                                                                                       | Significado                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt> </dl>             | Máscara usada para obtener el valor que se usa para invalidar el estado de presentación del recurso compartido DDE, si \_ \_ se establece NDDE Trust cmd \_ Show.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ CONFIAR en \_ cmd \_ Mostrar**</dt> <dt>0x10000000L</dt> </dl>          | Invalide el estado de la presentación especificado en el DSDM del recurso compartido DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ \_Recurso compartido \_ de confianza del**</dt> <dt>0x20000000L</dt> </dl>       | Quite el estado de confianza del recurso compartido.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L de inicio de \_ recurso \_ compartido de confianza**</dt> <dt></dt> </dl>    | Permita que un cliente se inicie en la aplicación si ya se está ejecutando en el contexto del usuario.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ \_ \_ Inicio del recurso compartido de confianza**</dt> <dt>0x80000000L</dt> </dl> | Permite que la aplicación se inicie en el contexto del usuario.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe la primera parte del identificador de modificación del recurso compartido de confianza. Este parámetro no puede ser **null**.

</dd> <dt>

*lpdwShareModId1* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe la segunda parte del identificador de modificación del recurso compartido de confianza. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

El identificador de modificación del recurso compartido de confianza refleja la versión del recurso compartido DDE en el DSDM en el momento en que se concedió inicialmente el estado de confianza al recurso compartido DDE. El identificador de modificación del recurso compartido de confianza se usa principalmente para quitar recursos compartidos de confianza obsoletos. Sin embargo, no es necesario que el usuario quite los recursos compartidos de confianza obsoletos. El agente DDE de red quita los recursos compartidos obsoletos en nombre del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) y **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




