---
title: Método INapSoHProcessor Initialize (NapProtocol.h)
description: Inicializa el paquete de protocolo y el sistema de procesador SoH. Se debe llamar a este método exactamente una vez.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Inicialización del método NAP
- Inicializar el método NAP , interfaz INapSoHProcessor
- INapSoHProcessor interface NAP , Initialize method
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
ms.openlocfilehash: c8279af6a58d23de762b077289688f32d07595b38998cf8644ff882ab2a6dcc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037845"
---
# <a name="inapsohprocessorinitialize-method"></a>INapSoHProcessor::Initialize (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHProcessor::Initialize** inicializa el paquete de protocolo y el sistema de procesador SoH. Se debe llamar a este método exactamente una vez.

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

*soh* \[ En\]
</dt> <dd>

Puntero al paquete [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) que se va a procesar.

</dd> <dt>

*isRequest* \[ En\]
</dt> <dd>

Un **VALOR BOOL** que es **TRUE** si el paquete es [**soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **FALSE** si es **soHResponse**.

</dd> <dt>

*id* \[ out\]
</dt> <dd>

[SystemHealthEntityId único](nap-datatypes.md) que contiene el identificador de SHA o SHV que construyó el paquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E PAQUETE NO \_ \_ VÁLIDO**</dt> </dl> | El paquete SoH no es válido.<br/>                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





