---
description: Consulta la cantidad de memoria libre en todos los montones de memoria de vídeo.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: Función NtGdiDdGetAvailDriverMemory (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c6ec322665b84b3ddad14b7032b8e49245377d40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080188"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a>NtGdiDdGetAvailDriverMemory función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Consulta la cantidad de memoria libre en todos los montones de memoria de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ de\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel creado previamente.

</dd> <dt>

*puGetAvailDriverMemoryData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [DD \_ GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) que contiene la información necesaria para realizar la consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdGetAvailDriverMemory** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




