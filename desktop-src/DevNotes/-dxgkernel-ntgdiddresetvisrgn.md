---
description: Se usa para permitir que el modo de usuario obtenga una descripción válida de la región de recorte para las ventanas del escritorio. Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos en modo de usuario.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Función NtGdiDdResetVisrgn (Ntgdi.h)
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
ms.openlocfilehash: 3077351b804f854520cff421fcad8a575278bb5a960f60ef760db38e7ca2f3a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833645"
---
# <a name="ntgdiddresetvisrgn-function"></a>Función NtGdiDdResetVisrgn

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Se usa para permitir que el modo de usuario obtenga una descripción válida de la región de recorte para las ventanas del escritorio. Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos en modo de usuario.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ En\]
</dt> <dd>

Puntero al objeto en modo de usuario de cualquier superficie que pertenezca al dispositivo DirectDraw para el que se va a restablecer el recorte. Para más información, consulte la documentación de DDK.

</dd> <dt>

*hwnd* \[ En\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **TRUE**; de lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

El recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos en modo de usuario. Las partes en modo kernel de DirectDraw y Windows Interfaz de dispositivo gráfico (GDI) mantienen un contador que se incrementa cada vez que cambia la lista de recorte para todo el escritorio. Una llamada a esta función registra este contador con todas las superficies principales existentes de DirectDraw en el sistema.

En cualquier momento posterior cuando una de estas superficies principales se modifica mediante una operación [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) (consulte la documentación del DDK), el contador registrado con la superficie se compara con el contador global. Si estos valores son diferentes, se devuelve un código de error DDERR \_ VISRGNCHANGED al código en modo de usuario. A continuación, el código en modo de usuario volverá a consultar el recorte actual del escritorio, llamará a **NtGdiDdResetVisrgn** y volverá a intentar el IDirectDrawSurface7::Blt aplicado a la superficie principal, respetando el nuevo recorte. Finalmente, el recorte muestreado por el código en modo de usuario será el mismo que el recorte actual que pertenece al modo kernel, y IDirectDrawSurface7::Blt podrá continuar.

Se recomienda a las aplicaciones usar la [interfaz IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o el método [IDirect3DDevice8::P resent](/previous-versions/ms889707(v=msdn.10)) para controlar los cambios de recorte asincrónicos. Estas construcciones implementan el recorte asincrónico de una manera automatizada e independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
