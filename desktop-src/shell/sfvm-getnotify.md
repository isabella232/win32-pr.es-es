---
description: Notificación enviada al objeto de devolución de llamada de vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios.
title: SFVM_GETNOTIFY mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267767"
---
# <a name="sfvm_getnotify-message"></a>Mensaje \_ GETNOTIFY de SFVM

Notificación enviada al objeto de devolución de llamada de vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios. Una vez registrados, cuando se produce un cambio en en estas ubicaciones o eventos, se notifica al objeto de devolución de llamada de vista. Estos eventos se envían a la devolución de llamada de vista a través de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) y, a continuación, se controlan mediante la vista.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidl* \[ out\]
</dt> <dd>

Puntero a un IDList absoluto de un elemento para el que la vista debe registrarse para recibir una notificación de los cambios. Normalmente, esto es lo mismo que idList de la ubicación que se está visualizando, pero puede ser otra ubicación.

> [!IMPORTANT]
> La duración de este valor pertenece al objeto de devolución de llamada de vista. Es responsabilidad del objeto de devolución de llamada de vista crear y, a continuación, liberar este valor cuando ya no sea necesario. Esto requiere que el objeto de devolución de llamada de vista almacena este valor. Normalmente, el valor se puede almacenar en el **\_ miembro pidlMonitor** del objeto de devolución de llamada de vista. Las reglas de propiedad para el valor devuelto *a través de pidl* no son estándar y requieren un cuidado especial. El objeto de devolución de llamada de vista debe poseer este valor y asegurarse de que no se libera hasta que se destruye el propio objeto de devolución de llamada de vista.

 

</dd> <dt>

*lEvents* \[ out\]
</dt> <dd>

Valor que contiene uno o varios valores SHCNE. Consulte [**SHChangeNotify para**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) obtener una lista de valores posibles. El objeto de devolución de llamada de vista se registrará para recibir un [**mensaje \_ FSNOTIFY**](sfvm-fsnotify.md) de SFVM cuando se produzca cualquiera de los eventos asociados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite, pero debe devolver S \_ OK.

## <a name="remarks"></a>Observaciones

Si este mensaje de devolución de llamada no devuelve un valor distinto de cero para IDList o la máscara de eventos, la vista no se registrará para las notificaciones de cambio.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una implementación de ejemplo del código de controlador de la función de devolución de llamada de vista **para SFVM \_ GETNOTIFY**.


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
