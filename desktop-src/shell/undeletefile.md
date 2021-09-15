---
description: Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos cuando el usuario elige el comando Undelete en el menú Archivo.
title: FM_UNDELETE_PROC de función (Wfext.h)
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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574501"
---
# <a name="fm_undelete_proc-function-pointer"></a>Puntero \_ de función FM UNDELETE \_ PROC

Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos cuando el usuario elige el comando **Undelete** en el **menú** Archivo.

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

Tipo: **HWND**

Identificador de ventana del Administrador de archivos. Un archivo DLL de recuperación debe usar este identificador para especificar la ventana de propietario de cualquier cuadro de diálogo o cuadro de mensaje que pueda mostrar el archivo DLL.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Tipo: **LPSTR**

Dirección de una cadena terminada en NULL que contiene el nombre del directorio inicial.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Devuelve uno de los valores siguientes.



| Código devuelto                                                                             | Descripción                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Se produjo un error.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Se ha eliminado un archivo. El Administrador de archivos vuelve a dibujar su ventana.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | No se ha eliminado ningún archivo.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




