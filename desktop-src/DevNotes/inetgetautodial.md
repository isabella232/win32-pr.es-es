---
description: La función InetGetAutodial devuelve la configuración de marcado automático del registro.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671399"
---
# <a name="inetgetautodial-function"></a>InetGetAutodial función)

\[Esta función no se admite y puede modificarse o no estar disponible en versiones futuras de Windows. \]

La función **InetGetAutodial** devuelve la configuración de marcado automático del registro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpfEnable* \[ enuncia\]
</dt> <dd>

Indica si el marcado automático está habilitado. Un valor de **true** cuando se devuelve indica que el marcado automático está habilitado.

</dd> <dt>

*lpszEntryName* \[ enuncia\]
</dt> <dd>

En la devolución, contiene el nombre de la entrada de la libreta de teléfonos que se establece para el marcado automático.

</dd> <dt>

*cbEntryNameSize* \[ de\]
</dt> <dd>

Tamaño del búfer asignado por el llamador para el nombre de la entrada de la libreta de teléfonos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                                | Descripción                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ correcto**</dt> </dl>              | La llamada se realizó correctamente.<br/>                                                                                                                       |
| <dl> <dt>**ERROR de \_ argumentos no válidos \_**</dt> </dl>       | *lpfEnable* o *lpszEntryName* contiene un puntero **nulo** o el valor de *cbEntryNameSize* es cero.<br/>                                         |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>  | Memoria insuficiente para asignar búferes internos.<br/>                                                                                    |
| <dl> <dt>**ERROR \_ de \_ búfer insuficiente**</dt> </dl> | *cbEntryNameSize* no indica que el búfer señalado por *lpszEntryName* es lo suficientemente grande como para recibir el nombre de la entrada de la libreta de teléfonos.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
