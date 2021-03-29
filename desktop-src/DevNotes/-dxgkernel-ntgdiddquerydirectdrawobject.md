---
description: Consulta una representación de modo kernel creada anteriormente de un objeto DirectDraw de Microsoft para sus capacidades.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Función NtGdiDdQueryDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907403"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>NtGdiDdQueryDirectDrawObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Consulta una representación de modo kernel creada anteriormente de un objeto DirectDraw de Microsoft para sus capacidades.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDrawLocal* \[ de\]
</dt> <dd>

Identificador del dispositivo DirectDraw en modo kernel creado previamente.

</dd> <dt>

*pHalInfo* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) que se rellenará con las funcionalidades del dispositivo. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Puntero a un búfer proporcionado por el autor de la llamada que almacena marcas de devolución de llamada detectadas por el controlador. El búfer debe tener el tamaño 3 \* (DWORD) y almacena las marcas de devolución de llamada en el orden siguiente: pCallBackFlags \[ 0 \] para las marcas en las [**\_ devoluciones de llamada de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 para las \] marcas en [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)y pCallBackFlags \[ 2 para las \] marcas en [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*puD3dCallbacks* \[ enuncia\]
</dt> <dd>

Puntero a una tabla de punteros de devolución de llamada de Direct3D. La tabla se rellena con punteros a funciones dentro de Gdi32.dll que imitan un controlador de pantalla de Direct3D. Esta tabla de devolución de llamada es idéntica a la estructura D3DHAL D3DCALLBACKS que se \_ describe en la documentación de DDK.

</dd> <dt>

*puD3dDriverData* \[ enuncia\]
</dt> <dd>

Puntero a los datos de [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , tal como se describe en la documentación de DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ enuncia\]
</dt> <dd>

Puntero a una tabla de punteros de devolución de llamada. La tabla se rellena con punteros a funciones dentro de Gdi32.dll que imitan un controlador de pantalla de Direct3D. Esta tabla de devolución de llamada es idéntica a la \_ estructura DDHAL DDEXEBUFCALLBACKS, que se asigna a la estructura [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) descrita en la documentación de DDK, salvo que los miembros XxxD3DBuffer en **DD \_ D3DBUFCALLBACKS** se reemplazan por XxxExecuteBuffer en DDHAL \_ DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de estructuras [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que definen el conjunto de formatos de textura permitidos.

</dd> <dt>

*puNumHeaps* \[ enuncia\]
</dt> <dd>

Puntero al miembro **dwNumHeaps** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. El miembro **dwNumHeaps** especifica el número de montones de memoria en *puvmList*. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*puvmList* \[ enuncia\]
</dt> <dd>

Puntero a una lista de descriptores del montón de memoria de vídeo. Puede ser **null**. Este parámetro no se usa porque la administración de la memoria de vídeo se controla completamente dentro del modo kernel.

</dd> <dt>

*puNumFourCC* \[ enuncia\]
</dt> <dd>

Puntero al miembro **puNumFourCCCodes** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. El miembro **puNumFourCCCodes** especifica el número de códigos de [cuatro caracteres (FourCC)](../directshow/fourcc-codes.md) que admite el controlador. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*puFourCC* \[ enuncia\]
</dt> <dd>

Puntero a una lista de formatos de superficie admitidos de [códigos de cuatro caracteres (FourCC)](../directshow/fourcc-codes.md) . Puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Una llamada a esta función está diseñada para realizarse en un proceso de dos pasos. En el primer paso, *puFourCC*, *puvmList* y *PuD3dTextureFormats* deben ser **null** y [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) se rellenará como [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** y [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con el número de entradas que se van a devolver. En la segunda llamada, el llamador debe asignar matrices del tamaño indicado y pasar esos punteros en lugar de valores **null** en los parámetros *puFourCC*, *puvmList* y *puD3dTextureFormats* . A continuación, las matrices se rellenarán con los datos adecuados.

Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos. Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
