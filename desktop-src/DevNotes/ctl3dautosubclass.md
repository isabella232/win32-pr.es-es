---
description: Subclases automáticamente y agrega efectos 3D a todos los cuadros de diálogo de la aplicación.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650103"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass función)

Subclases automáticamente y agrega efectos 3D a todos los cuadros de diálogo de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Identificador de la aplicación que se va a registrar como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** a menos que exista una de las condiciones siguientes, en cuyo caso devuelve **false**:

-   CTL3D se ejecuta en la versión 3,0 o anterior de Windows.
-   CTL3D no tiene espacio disponible en sus tablas para la aplicación actual. CTL3D puede atender hasta 32 aplicaciones al mismo tiempo.
-   CTL3D no puede instalar su enlace de CBT.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
