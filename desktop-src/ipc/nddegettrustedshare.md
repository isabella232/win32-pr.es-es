---
description: Recupera las opciones asociadas a un recurso compartido de DDE que se encuentra en la lista de usuarios del servidor de recursos compartidos de confianza.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Función NDdeGetTrustedShare (Nddeapi.h)
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
ms.openlocfilehash: 117178118f59c4f8830cab8aee6afc263d169bf58bac5ac81d3e33305b7db9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481935"
---
# <a name="nddegettrustedshare-function"></a>Función NDdeGetTrustedShare

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera las opciones asociadas a un recurso compartido de DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.

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

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*lpszShareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido cuyo estado de confianza se está consultando. Este parámetro no puede ser **NULL.**

</dd> <dt>

*lpdwTrustOptions* \[ out\]
</dt> <dd>

Puntero a una variable que recibe las opciones de confianza. Este parámetro no puede ser **NULL.** Están disponibles las siguientes opciones de confianza.



| Valor                                                                                                                                                                                                                                                       | Significado                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ SHOW \_ MASK**</dt> <dt>0x0000FFFFL</dt> </dl>             | Máscara usada para obtener el valor utilizado para invalidar el estado de presentación del recurso compartido de DDE, si se establece NDDE \_ TRUST \_ CMD \_ SHOW.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ CMD \_ SHOW**</dt> <dt>0x10000000L</dt> </dl>          | Invalide el estado de presentación especificado en DSDM del recurso compartido DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ DEL**</dt> <dt>0x20000000L</dt> </dl>       | Quite el estado de confianza del recurso compartido.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ INIT**</dt> <dt>0x40000000L</dt> </dl>    | Permitir que un cliente inicie en la aplicación si ya se está ejecutando en el contexto del usuario.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ START**</dt> <dt>0x80000000L</dt> </dl> | Permitir que la aplicación se inicia en el contexto del usuario.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ out\]
</dt> <dd>

Puntero a una variable que recibe la primera parte del identificador de modificación del recurso compartido de confianza. Este parámetro no puede ser **NULL.**

</dd> <dt>

*lpdwShareModId1* \[ out\]
</dt> <dd>

Puntero a una variable que recibe la segunda parte del identificador de modificación del recurso compartido de confianza. Este parámetro no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentarios

El identificador de modificación del recurso compartido de confianza refleja la versión del recurso compartido DDE en DSDM en el momento en que se concedió inicialmente el estado de confianza al recurso compartido de DDE. El identificador de modificación de recursos compartidos de confianza se usa principalmente para quitar recursos compartidos de confianza obsoletos. Sin embargo, el usuario no necesita quitar recursos compartidos de confianza obsoletos. El agente DDE de red quita los recursos compartidos obsoletos en nombre del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) y **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




