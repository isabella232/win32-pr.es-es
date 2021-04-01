---
title: Método Initialize INapSoHProcessor (NapProtocol. h)
description: Inicializa el paquete de protocolo y el sistema de procesador SoH. Se debe llamar a este método exactamente una vez.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996392"
---
# <a name="inapsohprocessorinitialize-method"></a>INapSoHProcessor:: Initialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHProcessor:: Initialize** inicializa el sistema del procesador SOH y el paquete de protocolo. Se debe llamar a este método exactamente una vez.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SOH* \[ de de\]
</dt> <dd>

Un puntero al paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) que se va a procesar.

</dd> <dt>

*isRequest* \[ de\]
</dt> <dd>

Valor **booleano** que es **true** si el paquete es un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si es un **SoHResponse**.

</dd> <dt>

*ID.* de \[ salida\]
</dt> <dd>

Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha o SHV que construyó el paquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**\_paquete NAP E \_ no válido \_**</dt> </dl> | El paquete SoH no es válido.<br/>                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





