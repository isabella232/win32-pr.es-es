---
description: El método configure envía información de configuración para una captura.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP:: Configure (método) (Netmon. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666269"
---
# <a name="iespconfigure-method"></a>IESP:: Configure (método)

El método **Configure** envía información de configuración para una captura.

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

Identificador de un BLOB de error que contiene información de error adicional. Para obtener información sobre el contenido de un BLOB de error, consulte la sección Comentarios de este tema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>                | NPP no está conectado a la red.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ no \_ ESP**</dt> </dl>                      | NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .<br/>                                                                                                         |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>                     | El NPP informa de que se ha iniciado la sesión de captura.<br/>                                                                                                                                                  |
| <dl> <dt>**\_desencadenador no válido de NMERR \_**</dt> </dl>              | La parte del desencadenador del BLOB de configuración está dañada.<br/>                                                                                                                                              |
| <dl> <dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt> </dl> | Falta una entrada necesaria para realizar esta operación en el BLOB de configuración especificado por *hConfigurationBlob* . Observe el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**\_error de \_ conversión de BLOB NMERR \_**</dt> </dl>       | El BLOB está dañado.<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_BLOB NMERR \_ no \_ inicializado**</dt> </dl>        | No se ha llamado al método **CreateBlob** .<br/>                                                                                                                                                         |
| <dl> <dt>**NMERR \_ BLOB no válido \_**</dt> </dl>                 | El objeto al que se apunta no es un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt> </dl>         | La cadena no termina en NULL.<br/>                                                                                                                                                                     |
| <dl> <dt>**\_BLOB de nivel superior de NMERR \_**</dt> </dl>                 | El número de versión del BLOB no es correcto.<br/>                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl>               | No había memoria disponible. Cierre Windows para liberar recursos.<br/>                                                                                                                                       |
| <dl> <dt>**tiempo de espera de NMERR \_**</dt> </dl>                       | La solicitud ha agotado el tiempo de espera.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado y detenido, pero no está desconectado.

El BLOB de error devuelto por el parámetro *hErrorBlob* contiene entradas que monitor de red no pudieron comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




