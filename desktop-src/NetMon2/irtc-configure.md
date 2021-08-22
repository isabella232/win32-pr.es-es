---
description: Envía datos de configuración para una captura de datos.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: Método IRTC::Configure (Netmon.h)
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
ms.openlocfilehash: 8f70674d8e570a2640fe301179b21a9f48ec612a17de69e43bdf5c38db4e65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063915"
---
# <a name="irtcconfigure-method"></a>IRTC::Configure (método)

El [**método Configure**](configure.md) envía datos de configuración para una captura de datos.

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

Identificador del BLOB configurado por el autor de la llamada.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Identificador de un blob de error que contiene datos de error adicionales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BLOB DE NMERR \_ \_ NO \_ INICIALIZADO**</dt> </dl>        | No se ha llamado al método **CreateBlob.**<br/>                                                                                                                                                 |
| <dl> <dt>**BLOB NO VÁLIDO DE NMERR \_ \_**</dt> </dl>                 | El objeto al que se apunta no es un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**BLOB DE NIVEL SUPERIOR \_ NMERR \_**</dt> </dl>                 | El número de versión de BLOB es incorrecto.<br/>                                                                                                                                                          |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ YA \_ \_ EXISTE**</dt> </dl>  | Blob duplicado.<br/>                                                                                                                                                                                |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ NO \_ \_ \_ EXISTE**</dt> </dl> | El BLOB de configuración especificado por *hConfigurationBlob* carece de una entrada necesaria para realizar esta operación. Vea el blob de error devuelto *por hErrorBlob para* determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**ESPECIFICADOR \_ AMBIGUO DE \_ NMERR**</dt> </dl>          | Faltan los datos Propietario de BLOB o Categoría.<br/>                                                                                                                                                    |
| <dl> <dt>**NO SE ENCONTRÓ EL \_ PROPIETARIO DEL BLOB \_ DE \_ \_ NMERR**</dt> </dl>       | No se encontró la sección Propietario del BLOB.<br/>                                                                                                                                                          |
| <dl> <dt>**NO SE ENCONTRÓ \_ LA CATEGORÍA DE BLOB \_ DE \_ NMERR \_**</dt> </dl>    | No se encontró la sección Categoría blob.<br/>                                                                                                                                                       |
| <dl> <dt>**CATEGORÍA DESCONOCIDA DE \_ \_ NMERR**</dt> </dl>             | Se encontró la sección Categoría BLOB, pero no se entiende.<br/>                                                                                                                                       |
| <dl> <dt>**ETIQUETA DESCONOCIDA DE NMERR \_ \_**</dt> </dl>                  | Se encontró la sección Etiqueta BLOB, pero no se entiende.<br/>                                                                                                                                            |
| <dl> <dt>**ERROR DE CONVERSIÓN \_ DE \_ BLOBS DE NMERR \_**</dt> </dl>       | El BLOB está dañado.<br/>                                                                                                                                                                           |
| <dl> <dt>**DESENCADENADOR NO ES DE NMERR \_ \_**</dt> </dl>              | La parte del desencadenador del BLOB está dañada.<br/>                                                                                                                                                    |
| <dl> <dt>**CADENA DE BLOB DE NMERR \_ \_ NO \_ VÁLIDA**</dt> </dl>         | La cadena no termina en NULL.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Comentarios

Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no desconectado.

El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El blob de error devuelto contiene datos de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Conectar](irtc-connect.md)
</dt> <dt>

[Monitor de red BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 




