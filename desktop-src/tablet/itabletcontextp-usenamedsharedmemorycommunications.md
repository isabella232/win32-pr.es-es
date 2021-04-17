---
description: Configura la comunicación de la memoria compartida para el contexto de la tableta.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'ITabletContextP:: UseNamedSharedMemoryCommunications (método)'
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
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716301"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>ITabletContextP:: UseNamedSharedMemoryCommunications (método)

Configura la comunicación de la memoria compartida para el contexto de la tableta.

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

*PID* \[ de de\]
</dt> <dd>

El ID. de proceso del cliente que tiene acceso a la memoria compartida.

</dd> <dt>

*pszCallerSid* \[ de\]
</dt> <dd>

El identificador de seguridad del autor de la llamada de función.

</dd> <dt>

*pszCallerIntegritySid* \[ de\]
</dt> <dd>

El identificador de seguridad que puede comprobar la integridad de la función de llamada.

</dd> <dt>

*pdwEventMoreDataId* \[ enuncia\]
</dt> <dd>

Entero que se usa para construir el nombre de un evento. El evento indica si hay más datos.

</dd> <dt>

*pdwEventClientReadyId* \[ enuncia\]
</dt> <dd>

Entero que se usa para construir el nombre de un evento. El evento indica que el cliente está listo para recibir datos. El evento se señala después de procesar los datos nuevos.

</dd> <dt>

*pdwMutexAccessId* \[ enuncia\]
</dt> <dd>

Puntero al identificador de acceso de la memoria compartida.

</dd> <dt>

*pdwFileMappingId* \[ enuncia\]
</dt> <dd>

Un entero que identifica la memoria compartida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El método **UseNamedSharedMemoryCommunications** forma parte del Protocolo de memoria compartida de Tablet PC. Un cliente sin privilegios elevados pasa en un identificador de seguridad (SID) y un identificador de seguridad de nivel de integridad (IL-SID) para que el servicio de tableta pueda utilizar listas de control de acceso (ACL) para tener acceso a los objetos de memoria compartida. Si el cliente tiene privilegios elevados, debe usar UseSharedMemoryCommunications, que es la API a la que se llama si el servicio ya tiene privilegios elevados.

La estructura del [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) almacena el encabezado de la memoria compartida.

La estructura del [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos. Los datos de paquete sin formato siguen el **\_ encabezado SHAREDMEMORY**. Los datos de paquetes sin formato se pueden leer en la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReadyId* .

En la lista siguiente se describe la secuencia de eventos para obtener acceso y usar la memoria compartida.

1.  El cliente genera el evento clientReady.
2.  El cliente espera el evento moreData.
3.  El cliente adquiere la exclusión mutua.
4.  El cliente Lee los datos de paquete de la sección de memoria compartida que sigue al encabezado. Los números de serie aparecen en la memoria compartida después de los datos del paquete.
5.  El cliente controla los datos en función del valor de **dwEvent**.
6.  El cliente escribe-1 (0xFFFFFFFF) en **dwEvent**.
7.  El cliente libera la exclusión mutua.
8.  El cliente genera el evento clientReady.

Los nombres de evento se crean dando formato al resultado de este método. Las siguientes definiciones se pueden usar junto con sprintf o su equivalente para crear los nombres de evento.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



En cada definición, la sección% d se reemplaza por el identificador de proceso y la sección% u se reemplaza por el entero devuelto en *pdwEventMoreDataId* o *pdwEventClientReadyId*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




