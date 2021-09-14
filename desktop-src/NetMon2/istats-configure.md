---
description: El método Configure envía información de configuración de captura.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: Método IStats::Configure (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071555"
---
# <a name="istatsconfigure-method"></a>IStats::Configure (método)

El **método Configure** envía información de configuración de captura.

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

Controlar un blob de error que contiene información de error adicional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CADENA DE BLOB DE NMERR \_ \_ NO \_ VÁLIDA**</dt> </dl>         | La cadena no termina en NULL.<br/>                                                                                                                                                                                            |
| <dl> <dt>**BLOB DE NMERR \_ \_ NO \_ INICIALIZADO**</dt> </dl>        | No se ha llamado al método **CreateBlob.**<br/>                                                                                                                                                                                |
| <dl> <dt>**BLOB NO VÁLIDO DE NMERR \_ \_**</dt> </dl>                 | El objeto al que se apunta no es un BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**BLOB DE \_ NMERR UPLEVEL \_**</dt> </dl>                 | El número de versión de BLOB es incorrecto.<br/>                                                                                                                                                                                         |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ YA \_ \_ EXISTE**</dt> </dl>  | Ya existe una entrada BLOB.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ NO \_ \_ \_ EXISTE**</dt> </dl> | El BLOB de configuración especificado por el *parámetro hConfigurationBlob* carece de una entrada necesaria para realizar esta operación. Mire el blob de error devuelto por el *parámetro hErrorBlob* para determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**ESPECIFICADOR \_ AMBIGUO DE \_ NMERR**</dt> </dl>          | El BLOB carece de información sobre el propietario o la categoría.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NO SE ENCONTRÓ EL \_ PROPIETARIO DEL BLOB DE NMERR \_ \_ \_**</dt> </dl>       | No se encontró la sección Propietario del BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**NO SE ENCONTRÓ \_ LA CATEGORÍA DE BLOB \_ DE \_ NMERR \_**</dt> </dl>    | No se encontró la sección Categoría del BLOB.<br/>                                                                                                                                                                               |
| <dl> <dt>**CATEGORÍA DESCONOCIDA DE NMERR \_ \_**</dt> </dl>             | Se encontró información de categoría, pero no se entiende.<br/>                                                                                                                                                                            |
| <dl> <dt>**ETIQUETA DESCONOCIDA DE NMERR \_ \_**</dt> </dl>                  | Se encontró información de etiqueta, pero no se entiende.<br/>                                                                                                                                                                                 |
| <dl> <dt>**ERROR DE CONVERSIÓN \_ DE \_ BLOBS DE NMERR \_**</dt> </dl>       | El BLOB está dañado.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**DESENCADENADOR NO ES DE NMERR \_ \_**</dt> </dl>              | La parte del desencadenador del BLOB está dañada.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido pero no desconectado.

El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender ni encontrar en el BLOB de configuración especificado en el *parámetro hConfigurationBlob.* El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[ISTATS::Conectar](istats-connect.md)
</dt> <dt>

[Monitor de red BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 




