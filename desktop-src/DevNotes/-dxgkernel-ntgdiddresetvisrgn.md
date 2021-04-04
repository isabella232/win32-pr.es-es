---
description: Se utiliza para habilitar el modo de usuario con el fin de obtener una descripción válida de la región de recorte para Windows en el escritorio. Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Función NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906972"
---
# <a name="ntgdiddresetvisrgn-function"></a>NtGdiDdResetVisrgn función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Se utiliza para habilitar el modo de usuario con el fin de obtener una descripción válida de la región de recorte para Windows en el escritorio. Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ de\]
</dt> <dd>

Puntero al objeto de modo de usuario de cualquier superficie que pertenezca al dispositivo DirectDraw para el que se va a restablecer el recorte. Para obtener más información, consulte la documentación de DDK.

</dd> <dt>

*hWnd* \[ de\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

El recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario. Las partes del modo kernel de DirectDraw y Windows Interfaz de dispositivo gráfico (GDI) mantienen un contador que se incrementa cada vez que cambia la lista de recortes para todo el escritorio. Una llamada a esta función registra este contador con todas las superficies principales de DirectDraw existentes en el sistema.

En cualquier momento posterior, cuando una de estas superficies principales se modifica mediante una operación [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (consulte la documentación del DDK), el contador registrado con la superficie se compara con el contador global. Si estos valores son diferentes, se devuelve un código de error DDERR \_ VISRGNCHANGED al código del modo de usuario. Después, el código de modo de usuario volverá a consultar el recorte actual del escritorio, llamará a **NtGdiDdResetVisrgn** y volverá a intentar el IDirectDrawSurface7:: BLT aplicado a la superficie primaria, respetando el nuevo recorte. Finalmente, el recorte que ha muestreado el código en modo de usuario será el mismo que el recorte actual propiedad del modo kernel y se permitirá que IDirectDrawSurface7:: BLT continúe.

Se recomienda a las aplicaciones que usen la interfaz [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o [IDirect3DDevice8::P método reenviado](/previous-versions/ms889707(v=msdn.10)) para controlar los cambios de recorte asincrónicos. Estas construcciones implementan el recorte asincrónico de una forma independiente del sistema operativo y automatizada.

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

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
