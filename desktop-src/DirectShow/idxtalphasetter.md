---
description: La interfaz IDxtAlphaSetter establece propiedades en el efecto Alfa Setter. Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa el efecto Alfa Setter.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaz IDxtAlphaSetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362418"
---
# <a name="idxtalphasetter-interface"></a>Interfaz IDxtAlphaSetter

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IDxtAlphaSetter` interfaz establece las propiedades en el efecto Alfa [Setter.](alpha-setter-effect.md)

Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa el efecto Alfa Setter. Las aplicaciones DES no tienen que usar esta interfaz. Para establecer las propiedades en una transición en DES, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Members

La **interfaz IDxtAlphaSetter** hereda de **IDXEffect**. **IDxtAlphaSetter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDxtAlphaSetter tiene** estos métodos.



| Método                                                  | Descripción                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**get \_ Alpha**](idxtalphasetter-get-alpha.md)         | Recupera el valor alfa de toda la imagen.<br/> |
| [**get \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera la propiedad de rampa alfa.<br/>              |
| [**put \_ Alpha**](idxtalphasetter-put-alpha.md)         | Especifica el valor alfa para toda la imagen.<br/> |
| [**put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Especifica la propiedad de rampa alfa.<br/>              |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




