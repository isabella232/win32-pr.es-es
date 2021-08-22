---
title: Función de devolución de llamada PxeProviderInitialize
description: Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Función de devolución de llamada PxeProviderInitialize Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098665"
---
# <a name="pxeproviderinitialize-callback-function"></a>Función de devolución de llamada PxeProviderInitialize

Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente. Los proveedores deben exportar la *función PxeProviderInitialize.* Las devoluciones de llamada al proveedor deben registrarse con una llamada a la [**función PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante el procesamiento de *PxeProviderInitialize*. A la devolución de esta función, el proveedor debe estar totalmente inicializado y listo para procesar las solicitudes de cliente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor. El proveedor debe almacenar este identificador y usarse en las llamadas posteriores. Este identificador es válido hasta que se llama a la función de devolución de llamada [*PxeProviderShutdown.*](pxeprovidershutdown.md)

</dd> <dt>

*hProviderKey* \[ En\]
</dt> <dd>

Identificador de una clave del Registro donde se va a almacenar la información de configuración del proveedor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la inicialización del proveedor se realiza correctamente, la devolución de llamada debe devolver **ERROR \_ SUCCESS**. En caso de error, se debe devolver un código de error adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 solo con aplicaciones de escritorio sp2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Funciones del servidor de Servicios de implementación](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





