---
description: La interfaz IDxtKey establece las propiedades en la transición de clave. Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de clave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaz IDxtKey (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d967d15dededf879ffd08671aac00e7892aa8ad2f2c1a39ce478f7f9f3e4db90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792365"
---
# <a name="idxtkey-interface"></a>Interfaz IDxtKey

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IDxtKey` interfaz establece las propiedades en la transición [de](key-transition.md) clave.

Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de clave. Las aplicaciones DES no necesitan usar esta interfaz. Para establecer las propiedades en una transición en DES, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Miembros

La **interfaz IDxtKey** hereda de **IDXEffect**. **IDxtKey** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDxtKey** tiene estos métodos.



| Método                                            | Descripción                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**get \_ Hue**](idxtkey-get-hue.md)               | Recupera el valor de matiz en el que se va a claver.<br/>                                    |
| [**get \_ Invert**](idxtkey-get-invert.md)         | Recupera un valor booleano que indica si se invierte la operación de clave.<br/> |
| [**get \_ KeyType**](idxtkey-get-keytype.md)       | Recupera el tipo de clave.<br/>                                                  |
| [**get \_ Luminance**](idxtkey-get-luminance.md)   | Recupera el valor de luminosidad en el que se va a claver.<br/>                              |
| [**get \_ RGB**](idxtkey-get-rgb.md)               | Recupera el color RGB en el que se va a claver.<br/>                                    |
| [**obtener \_ similitud**](idxtkey-get-similarity.md) | Recupera el intervalo de datos de color que se vuelve transparente.<br/>                 |
| [**put \_ Hue**](idxtkey-put-hue.md)               | Especifica el valor de matiz en el que se va a claver.<br/>                                    |
| [**put \_ Invert**](idxtkey-put-invert.md)         | Especifica si se invierte la operación de clave.<br/>                            |
| [**put \_ KeyType**](idxtkey-put-keytype.md)       | Especifica el tipo de clave.<br/>                                                  |
| [**put \_ Luminance**](idxtkey-put-luminance.md)   | Especifica el valor de luminosidad en el que se va a claver.<br/>                              |
| [**put \_ RGB**](idxtkey-put-rgb.md)               | Especifica el color RGB en el que se va a claver.<br/>                                    |
| [**put \_ Similarity**](idxtkey-put-similarity.md) | Especifica el intervalo de datos de color que se vuelve transparente.<br/>                 |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




