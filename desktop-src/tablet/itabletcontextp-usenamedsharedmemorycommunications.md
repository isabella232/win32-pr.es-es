---
description: Configura la comunicación de memoria compartida para el contexto de la tableta.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: Método ITabletContextP::UseNamedSharedMemoryCommunications
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: a8ce5d4dde7f3fd678e4ac748a0f148750344a1e5e8da9f6481ad25eafa016a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712235"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>Método ITabletContextP::UseNamedSharedMemoryCommunications

Configura la comunicación de memoria compartida para el contexto de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pid* \[ En\]
</dt> <dd>

Identificador de proceso del cliente que tiene acceso a la memoria compartida.

</dd> <dt>

*pszCallerSid* \[ En\]
</dt> <dd>

Identificador de seguridad del llamador de función.

</dd> <dt>

*pszCallerIntegritySid* \[ En\]
</dt> <dd>

Identificador de seguridad que puede comprobar la integridad de la función que realiza la llamada.

</dd> <dt>

*pdwEventMoreDataId* \[ out\]
</dt> <dd>

Entero que se usa para construir el nombre de un evento. El evento indica si hay más datos.

</dd> <dt>

*pdwEventClientReadyId* \[ out\]
</dt> <dd>

Entero que se usa para construir el nombre de un evento. El evento indica que el cliente está listo para recibir datos. El evento se señala después de procesar nuevos datos.

</dd> <dt>

*pdwMutexAccessId* \[ out\]
</dt> <dd>

Puntero al identificador de acceso de la memoria compartida.

</dd> <dt>

*pdwFileMappingId* \[ out\]
</dt> <dd>

Entero que identifica la memoria compartida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **método UseNamedSharedMemoryCommunications** forma parte del protocolo de memoria compartida de Tablet PC. Un cliente sin privilegios elevados pasa un identificador de seguridad (SID) y un identificador de seguridad de nivel de integridad (IL-SID) para que tablet service pueda usar listas de control de acceso (ACL) para acceder a los objetos de memoria compartida. Si el cliente tiene privilegios elevados, debe usar UseSharedMemoryCommunications, que es la API a la que se llama si el servicio ya tiene un privilegio elevado.

La [**estructura SHAREDMEMORY \_ HEADER**](sharedmemory-header.md) almacena el encabezado de memoria compartida.

La [**estructura SHAREDMEMORY \_ HEADER**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos. Los datos de paquetes sin procesar siguen **al ENCABEZADO SHAREDMEMORY \_**. Los datos de paquetes sin procesar se pueden leer de la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReadyId.*

En la lista siguiente se describe la secuencia de eventos para acceder a la memoria compartida y usarla.

1.  El cliente genera el evento clientReady.
2.  El cliente espera el evento moreData.
3.  El cliente adquiere la exclusión mutua.
4.  El cliente lee los datos de paquetes de la sección de memoria compartida que sigue al encabezado . Los números de serie aparecen en la memoria compartida después de los datos del paquete.
5.  El cliente controla los datos en función del valor **de dwEvent**.
6.  El cliente escribe -1 (0xFFFFFFFF) en **dwEvent**.
7.  El cliente libera la exclusión mutua.
8.  El cliente genera el evento clientReady.

Los nombres de evento se crean mediante el formato de la salida de este método. Las siguientes definiciones se pueden usar junto con sprintf o su equivalente para crear los nombres de evento.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



En cada definición, la sección %d se reemplaza por el identificador de proceso y la sección %u se reemplaza por el entero devuelto en *pdwEventMoreDataId* o *pdwEventClientReadyId*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




