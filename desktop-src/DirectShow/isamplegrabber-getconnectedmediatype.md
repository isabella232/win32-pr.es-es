---
description: El método GetConnectedMediaType recupera el tipo de medio para la conexión en el pin de entrada del sample grabber.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: Método ISampleGrabber::GetConnectedMediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818064"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>ISampleGrabber::GetConnectedMediaType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetConnectedMediaType` método recupera el tipo de medio para la conexión en la patilla de entrada del sample grabber.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pType* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada por el autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                           | Descripción                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Argumento de** puntero NULL.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método copia el tipo de medio en la **estructura \_ AM MEDIA \_ TYPE** especificada por *pType*. El autor de la llamada debe liberar el bloque de formato del tipo de medio. Puede usar la **función CoTaskMemFree** o [**la función FreeMediaType**](freemediatype.md) en la biblioteca de clase base.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de Sample Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber (interfaz)**](isamplegrabber.md)
</dt> </dl>

 

 




