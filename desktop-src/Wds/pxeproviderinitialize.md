---
title: Función de devolución de llamada PxeProviderInitialize
description: Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Función de devolución de llamada PxeProviderInitialize servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705185"
---
# <a name="pxeproviderinitialize-callback-function"></a>Función de devolución de llamada PxeProviderInitialize

Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente. Los proveedores son necesarios para exportar la función *PxeProviderInitialize* . Todas las devoluciones de llamada al proveedor se deben registrar con una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante el procesamiento de *PxeProviderInitialize*. En la devolución de esta función, el proveedor debe inicializarse completamente y estar listo para procesar solicitudes de cliente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor. Este identificador debe almacenarse por el proveedor y usarse en cualquier llamada subsiguiente. Este identificador es válido hasta que se llama a la función de devolución de llamada [*PxeProviderShutdown*](pxeprovidershutdown.md) .

</dd> <dt>

*hProviderKey* \[ de\]
</dt> <dd>

Identificador de una clave del registro en la que se va a almacenar la información de configuración del proveedor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la inicialización del proveedor se realiza correctamente, la devolución de llamada debe devolver el **error \_ correcto**. En caso de error, se debe devolver un código de error adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de servidor de servicios de implementación de Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





