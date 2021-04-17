---
description: Proporciona acceso a la memoria compartida entre los subprocesos de tableta.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'ITabletContextP:: UseSharedMemoryCommunications (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717158"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>ITabletContextP:: UseSharedMemoryCommunications (método)

Proporciona acceso a la memoria compartida entre los subprocesos de tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PID* \[ de de\]
</dt> <dd>

Identificador de proceso.

</dd> <dt>

*phEventMoreData* \[ enuncia\]
</dt> <dd>

Identificador de evento que indica cuándo están disponibles los nuevos datos para su procesamiento.

</dd> <dt>

*phEventClientReady* \[ enuncia\]
</dt> <dd>

Identificador de evento devuelto que se usa para indicar que el cliente está listo para recibir datos. Señalado después del procesamiento de datos nuevos.

</dd> <dt>

*phMutexAccess* \[ enuncia\]
</dt> <dd>

La exclusión mutua que concede acceso a la memoria compartida.

</dd> <dt>

*phFileMapping* \[ enuncia\]
</dt> <dd>

Puntero al bloque de memoria compartida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El método **UseSharedMemoryCommunications** se usa como parte del Protocolo de memoria compartida de Tablet PC. Dado que el servicio Wisptis tiene un nivel de integridad alto (IL), puede almacenar y obtener acceso a los datos almacenados en la memoria compartida sin necesidad de elevar sus privilegios.

La estructura de [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos y los datos de paquete sin formato siguen el **\_ encabezado SHAREDMEMORY**. Los datos de paquetes sin formato se pueden leer en la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReady* .

En la lista siguiente se describe la secuencia de eventos para obtener acceso y usar la memoria compartida.

-   El cliente establece el evento clientReady.
-   El cliente espera el evento moreData.
-   El cliente adquiere la exclusión mutua.
-   El cliente Lee los datos de paquetes de la sección de memoria compartida después del encabezado y los números de serie después de los paquetes.
-   El cliente controla los datos en función del valor de **dwEvent**.
-   El cliente escribe-1 (0xFFFFFFFF) en **dwEvent**.
-   El cliente libera la exclusión mutua.
-   El cliente establece el evento clientReady.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




