---
description: El método Configure envía información de configuración para una captura.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: Método IESP::Configure (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476721"
---
# <a name="iespconfigure-method"></a>IESP::Configure (método)

El **método Configure** envía información de configuración para una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConfigurationBlob* \[ En\]
</dt> <dd>

Controle el BLOB que configura el autor de la llamada.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Controlar un blob de error que contiene información de error adicional. Para obtener información sobre el contenido de un BLOB de error, vea la sección Comentarios de este tema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>                | El NPP no está conectado a la red.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>                      | El NPP está conectado a la red, pero no con el [método IESP::Conectar.](iesp-connect.md)<br/>                                                                                                         |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>                     | El NPP informa de que se ha iniciado la sesión de captura.<br/>                                                                                                                                                  |
| <dl> <dt>**DESENCADENADOR NO ES DE NMERR \_ \_**</dt> </dl>              | La parte del desencadenador del BLOB de configuración está dañada.<br/>                                                                                                                                              |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ NO \_ \_ \_ EXISTE**</dt> </dl> | Al BLOB de configuración especificado por *hConfigurationBlob* le falta una entrada necesaria para realizar esta operación. Mire el blob de error devuelto por *hErrorBlob para* determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**ERROR DE CONVERSIÓN \_ DE \_ BLOBS DE NMERR \_**</dt> </dl>       | El BLOB está dañado.<br/>                                                                                                                                                                                   |
| <dl> <dt>**BLOB DE NMERR \_ \_ NO \_ INICIALIZADO**</dt> </dl>        | No se ha llamado al método **CreateBlob.**<br/>                                                                                                                                                         |
| <dl> <dt>**BLOB NO VÁLIDO DE NMERR \_ \_**</dt> </dl>                 | El objeto al que se apunta no es un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**CADENA DE BLOB DE NMERR \_ \_ NO \_ VÁLIDA**</dt> </dl>         | La cadena no termina en NULL.<br/>                                                                                                                                                                     |
| <dl> <dt>**BLOB DE \_ NMERR UPLEVEL \_**</dt> </dl>                 | El número de versión de BLOB es incorrecto.<br/>                                                                                                                                                                  |
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl>               | No había memoria disponible. Apague las ventanas para liberar recursos.<br/>                                                                                                                                       |
| <dl> <dt>**TIEMPO DE ESPERA de NMERR \_**</dt> </dl>                       | La solicitud ha agotado el tiempo de espera.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado y detenido, pero que no está desconectado.

El blob de error devuelto por el parámetro *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender ni encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




