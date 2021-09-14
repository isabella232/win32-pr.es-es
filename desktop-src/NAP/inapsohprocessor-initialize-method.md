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
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071665"
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
| Encabezado<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





