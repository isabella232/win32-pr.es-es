---
description: Proporciona acceso a la memoria compartida entre subprocesos de tableta.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: Método ITabletContextP::UseSharedMemoryCommunications
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579461"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>Método ITabletContextP::UseSharedMemoryCommunications

Proporciona acceso a la memoria compartida entre subprocesos de tableta.

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

*pid* \[ En\]
</dt> <dd>

Id. de proceso.

</dd> <dt>

*phEventMoreData* \[ out\]
</dt> <dd>

Identificador de eventos que indica cuándo hay nuevos datos disponibles para procesarse.

</dd> <dt>

*phEventClientReady* \[ out\]
</dt> <dd>

Identificador de evento devuelto que se usa para indicar que el cliente está listo para recibir datos. Se señala después de procesar nuevos datos.

</dd> <dt>

*phMutexAccess* \[ out\]
</dt> <dd>

Exclusión mutua que concede acceso a la memoria compartida.

</dd> <dt>

*phFileMapping* \[ out\]
</dt> <dd>

Puntero al bloque de memoria compartida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El **método UseSharedMemoryCommunications** se usa como parte del protocolo de memoria compartida de Tablet PC. Dado que el servicio Wisptis tiene un alto nivel de integridad (IL), puede almacenar y acceder a los datos almacenados en memoria compartida sin necesidad de elevar sus privilegios.

La [**estructura SHAREDMEMORY \_ HEADER**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos y los datos de paquetes sin procesar siguen **a SHAREDMEMORY \_ HEADER**. Los datos de paquetes sin procesar se pueden leer de la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReady.*

En la lista siguiente se describe la secuencia de eventos para acceder a la memoria compartida y usarla.

-   El cliente establece el evento clientReady.
-   El cliente espera el evento moreData.
-   El cliente adquiere la exclusión mutua.
-   El cliente lee los datos de paquetes de la sección de memoria compartida después del encabezado y los números de serie después de los paquetes.
-   El cliente controla los datos en función del valor **de dwEvent**.
-   El cliente escribe -1 (0xFFFFFFFF) en **dwEvent**.
-   El cliente libera la exclusión mutua.
-   El cliente establece el evento clientReady.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletContextP (interfaz)**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




