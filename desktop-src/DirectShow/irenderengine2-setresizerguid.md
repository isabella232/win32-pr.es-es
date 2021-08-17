---
description: El método SetResizerGUID especifica el CLSID de un filtro de tamaño de vídeo personalizado.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: Método IRenderEngine2::SetResizerGUID (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e650a250333ac784e599d0bce820ef390a937f49bff2371b1b7a52b18d9d0ad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818540"
---
# <a name="irenderengine2setresizerguid-method"></a>IRenderEngine2::SetResizerGUID (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetResizerGUID` método especifica el CLSID de un filtro de tamaño de vídeo personalizado. Llame a este método para reemplazar el filtro de tamaño predeterminado que usa DirectShow Editing Services. El filtro debe estar registrado como un objeto COM en el sistema del usuario y debe admitir la [**interfaz IResize.**](iresize.md)

Llame a este método antes de llamar [**a IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResizerGuid* \[ En\]
</dt> <dd>

CLSID del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Para revertir al cambio de tamaño de DES predeterminado, use el siguiente CLSID:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IRenderEngine2**](irenderengine2.md)
</dt> </dl>

 

 




