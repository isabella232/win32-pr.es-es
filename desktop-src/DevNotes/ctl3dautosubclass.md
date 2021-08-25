---
description: Crea automáticamente subclases y agrega efectos 3D a todos los cuadros de diálogo de la aplicación.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Función Ctl3dAutoSubclass
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
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654615"
---
# <a name="ctl3dautosubclass-function"></a>Función Ctl3dAutoSubclass

Crea automáticamente subclases y agrega efectos 3D a todos los cuadros de diálogo de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prendstApp* 
</dt> <dd>

Identificador de la aplicación que se va a registrar como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** a menos que exista una de las condiciones siguientes, en cuyo caso devuelve **FALSE**:

-   CTL3D se ejecuta en Windows versión 3.0 o anterior.
-   CTL3D no tiene espacio disponible en sus tablas para la aplicación actual. CTL3D puede dar servicio a hasta 32 aplicaciones al mismo tiempo.
-   CTL3D no puede instalar su enlace CBT.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
