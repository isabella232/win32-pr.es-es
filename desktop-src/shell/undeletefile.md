---
description: Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando Undelete en el menú archivo.
title: FM_UNDELETE_PROC puntero a función (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278863"
---
# <a name="fm_undelete_proc-function-pointer"></a>\_Puntero de función de procedimiento de eliminación de FM \_

Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando **Undelete** en el menú **archivo** .

## <a name="syntax"></a>Sintaxis


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndOwner* 
</dt> <dd>

Tipo: **hWnd**

Identificador de ventana para el administrador de archivos. Un archivo DLL de deseliminación debe usar este identificador para especificar la ventana propietaria de cualquier cuadro de diálogo o cuadro de mensaje que el archivo DLL puede mostrar.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Tipo: **LPSTR**

Dirección de una cadena terminada en null que contiene el nombre del directorio inicial.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Devuelve uno de los valores siguientes.



| Código devuelto                                                                             | Descripción                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Se produjo un error.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Se ha cancelado la eliminación de un archivo. El administrador de archivos vuelve a dibujar su ventana.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | No se eliminó ningún archivo.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




