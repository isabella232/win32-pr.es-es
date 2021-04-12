---
title: Método Initialize INapEnforcementClientBinding (NapEnforcementClient. h)
description: Inicia automáticamente el servicio NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489892"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>INapEnforcementClientBinding:: Initialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientBinding:: Initialize** inicia el servicio NapAgent automáticamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Un [**EnforcementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento y su versión.

</dd> <dt>

*devolución de llamada* \[ de\]
</dt> <dd>

Puntero COM a una interfaz [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) que usa NapAgent para devolver la llamada a los clientes de cumplimiento con Notify/Process. NapAgent contiene una referencia al objeto asociado a esta interfaz hasta que se llama a [**INapEnforcementClientBinding:: UnInitialize**](inapenforcementclientbinding-uninitialize-method.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                                         | Descripción                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                               | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>                     | Error de permisos, acceso denegado.<br/>                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                      | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                       |
| <dl> <dt>**HRESULT (ERROR \_ ya \_ inicializado)**</dt> </dl> | Si el aplicador se ha inicializado previamente, se devuelve este código de error.<br/> |
| <dl> <dt>**NAP \_ E \_ no \_ registrado**</dt> </dl>              | Si el aplicador no se ha registrado anteriormente, se devuelve este código de error.<br/>      |



 

## <a name="remarks"></a>Observaciones

El cliente de cumplimiento debe llamar al método **INapEnforcementClientBinding:: Initialize** antes de llamar a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding:: UnInitialize**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





