---
description: Notificación enviada al objeto de devolución de llamada de la vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios.
title: Mensaje de SFVM_GETNOTIFY (ShlObj. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277638"
---
# <a name="sfvm_getnotify-message"></a>SFVM \_ GETNOTIFY

Notificación enviada al objeto de devolución de llamada de la vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios. Una vez que se registran, cuando se produce un cambio en en estas ubicaciones o eventos, se notifica el objeto de devolución de llamada de la vista. Estos eventos se envían a la devolución de llamada de la vista a través de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) y, a continuación, se controlan mediante la vista.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PIDL* \[ enuncia\]
</dt> <dd>

Un puntero a un IDList absoluto de un elemento para el que la vista debe registrarse para recibir notificaciones de los cambios. Normalmente, es el mismo que el IDList de la ubicación que se está viendo, pero puede ser otra ubicación.

> [!IMPORTANT]
> La duración de este valor es propiedad del objeto de devolución de llamada de la vista. Es responsabilidad del objeto de devolución de llamada de la vista crear y, a continuación, liberar este valor cuando ya no se necesite. Esto requiere que el objeto de devolución de llamada de la vista almacene este valor. Normalmente, el valor se puede almacenar en el miembro **\_ pidlMonitor** del objeto de devolución de llamada de la vista. Las reglas de propiedad para el valor devuelto a través de *PIDL* son no estándar y requieren especial atención. El objeto de devolución de llamada de vista debe poseer este valor y asegurarse de que no se libera hasta que se destruye el propio objeto de devolución de llamada de la vista.

 

</dd> <dt>

*lEvents* \[ enuncia\]
</dt> <dd>

Valor que contiene uno o más valores de SHCNE. Consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para obtener una lista de los valores posibles. El objeto de devolución de llamada de vista se registrará para recibir un mensaje de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) cuando se produce cualquiera de los eventos asociados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite, pero debe devolver S \_ correcto.

## <a name="remarks"></a>Observaciones

Si este mensaje de devolución de llamada no devuelve un valor distinto de cero para IDList o la máscara de eventos, la vista no se registrará para las notificaciones de cambio.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra una implementación de ejemplo del código de controlador de la función de devolución de llamada de vista para **SFVM \_ GETNOTIFY**.


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
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
