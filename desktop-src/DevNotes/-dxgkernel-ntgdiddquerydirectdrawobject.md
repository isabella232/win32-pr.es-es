---
description: Consulta una representación en modo kernel creada previamente de un objeto Microsoft DirectDraw para sus funcionalidades.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Función NtGdiDdQueryDirectDrawObject (Ntgdi.h)
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
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103825"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>Función NtGdiDdQueryDirectDrawObject

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Consulta una representación en modo kernel creada previamente de un objeto Microsoft DirectDraw para sus funcionalidades.

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

*hDirectDrawLocal* \[ En\]
</dt> <dd>

Controle el dispositivo DirectDraw en modo kernel creado anteriormente.

</dd> <dt>

*pHalInfo* \[ out\]
</dt> <dd>

Puntero a una [**estructura \_ DD HOLINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) que se rellenará con las funcionalidades del dispositivo. Consulte la documentación de DDK para más información.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Puntero a un búfer proporcionado por el autor de la llamada que almacena las marcas de devolución de llamada notificadas por el controlador. El búfer debe tener el tamaño 3 sizeof(DWORD) y almacena las marcas de devolución de llamada en el orden siguiente: pCallBackFlags 0 para las marcas en \* \[ \] [**DD \_ CALLBACKS,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks)pCallBackFlags 1 para las marcas en \[ \] [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)y pCallBackFlags 2 para las marcas en \[ \] [**DD \_ PALETTECALLBACKS.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks) Consulte la documentación de DDK para más información.

</dd> <dt>

*puD3dCallbacks* \[ out\]
</dt> <dd>

Puntero a una tabla de punteros de devolución de llamada de Direct3D. La tabla se rellena con punteros a funciones dentro Gdi32.dll que imitan un controlador de pantalla de Direct3D. Esta tabla de devolución de llamada es idéntica a la estructura \_ D3DHAL D3DCALLBACKS que se describe en la documentación de DDK.

</dd> <dt>

*puD3dDriverData* \[ out\]
</dt> <dd>

Puntero a [**datos D3DHAL \_ GLOBALDRIVERDATA,**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) como se describe en la documentación de DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ out\]
</dt> <dd>

Puntero a una tabla de punteros de devolución de llamada. La tabla se rellena con punteros a funciones dentro Gdi32.dll que imitan un controlador de pantalla de Direct3D. Esta tabla de devolución de llamada es idéntica a la estructura DDHAL DDEXEBUFCALLBACKS, que se asigna a la estructura \_ [**\_ DD D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) que se describe en la documentación del DDK, salvo que los miembros XxxD3DBuffer de **DD \_ D3DBUFCALLBACKS** se reemplazan por XxxExecuteBuffer en DDHAL \_ DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ out\]
</dt> <dd>

Puntero a una matriz de [**estructuras DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que definen el conjunto de formatos de textura permitidos.

</dd> <dt>

*puNumHeaps* \[ out\]
</dt> <dd>

Puntero al **miembro dwNumHeaps** [**de \_ DDCUEINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. El **miembro dwNumHeaps** especifica el número de montones de memoria en *puvmList.* Consulte la documentación de DDK para más información.

</dd> <dt>

*puvmList* \[ out\]
</dt> <dd>

Puntero a una lista de descriptores de montón de memoria de vídeo. Puede ser **NULL.** Este parámetro no se usa porque la administración de memoria de vídeo se controla completamente en modo kernel.

</dd> <dt>

*puNumFourCC* \[ out\]
</dt> <dd>

Puntero al **miembro puNumFourCCCodes** [**de \_ DDFAINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. El **miembro puNumFourCCCodes** especifica el número de códigos de cuatro caracteres [(FOURCC)](../directshow/fourcc-codes.md) que admite el controlador. Consulte la documentación de DDK para más información.

</dd> <dt>

*puFourCC* \[ out\]
</dt> <dd>

Puntero a una lista de formatos de superficie de códigos de cuatro caracteres [(FOURCC)](../directshow/fourcc-codes.md) admitidos. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **TRUE**; de lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

Una llamada a esta función está diseñada para realizarse en un proceso de dos pasos. En el primer paso, *puFourCC,* *puvmList* y *puD3dTextureFormats* deben ser **NULL** y [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) rellenará [**\_ DDOBJINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. **dwNumFourCCCodes,** **DD \_ SEOINFO**.**vmiData**. **dwNumHeaps** y [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con el número de entradas que se van a devolver. En la segunda llamada, el autor de la llamada debe asignar matrices del tamaño indicado y pasar esos punteros en lugar de valores **NULL** en los parámetros *puFourCC,* *puvmList* y *puD3dTextureFormats.* A continuación, las matrices se rellenarán con los datos adecuados.

Se recomienda a las aplicaciones usar las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivos gráficos. Estas construcciones abstrae el proceso de creación de dispositivos de una manera simplificada e independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
