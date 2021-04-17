---
description: Envía datos de configuración para una captura de datos.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC:: Configure (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652403"
---
# <a name="irtcconfigure-method"></a>IRTC:: Configure (método)

El método [**Configure**](configure.md) envía datos de configuración para una captura de datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConfigurationBlob* \[ de\]
</dt> <dd>

Identificador del BLOB que el autor de la llamada configura.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error que contiene datos de error adicionales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_BLOB NMERR \_ no \_ inicializado**</dt> </dl>        | No se ha llamado al método **CreateBlob** .<br/>                                                                                                                                                 |
| <dl> <dt>**NMERR \_ BLOB no válido \_**</dt> </dl>                 | El objeto al que apunta no es un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**\_BLOB de nivel superior de NMERR \_**</dt> </dl>                 | El número de versión del BLOB no es correcto.<br/>                                                                                                                                                          |
| <dl> <dt>**la \_ entrada de BLOB NMERR \_ \_ ya \_ existe**</dt> </dl>  | BLOB duplicado.<br/>                                                                                                                                                                                |
| <dl> <dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt> </dl> | El BLOB de configuración especificado por *hConfigurationBlob* no tiene una entrada necesaria para realizar esta operación. Vea el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**NMERR \_ ( \_ especificador ambiguo)**</dt> </dl>          | Faltan los datos de la categoría o del propietario del BLOB.<br/>                                                                                                                                                    |
| <dl> <dt>**\_ \_ \_ no \_ se encontró el propietario del BLOB de NMERR**</dt> </dl>       | No se encontró la sección del propietario del BLOB.<br/>                                                                                                                                                          |
| <dl> <dt>**\_ \_ \_ no \_ se encontró la categoría de BLOB NMERR**</dt> </dl>    | No se encontró la sección de categoría de BLOB.<br/>                                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ categoría desconocida**</dt> </dl>             | Se encontró la sección de la categoría BLOB, pero no se entendió.<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ etiqueta desconocida**</dt> </dl>                  | La sección de etiqueta de BLOB se encontró, pero no se entendió.<br/>                                                                                                                                            |
| <dl> <dt>**\_error de \_ conversión de BLOB NMERR \_**</dt> </dl>       | El BLOB está dañado.<br/>                                                                                                                                                                           |
| <dl> <dt>**\_desencadenador no válido de NMERR \_**</dt> </dl>              | La parte del desencadenador del BLOB está dañada.<br/>                                                                                                                                                    |
| <dl> <dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt> </dl>         | La cadena no termina en NULL.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no está desconectado.

El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El BLOB de error devuelto contiene datos de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no se puede encontrar se incluye en el BLOB de error devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[BLOBs Monitor de red](network-monitor-blobs.md)
</dt> </dl>

 

 




