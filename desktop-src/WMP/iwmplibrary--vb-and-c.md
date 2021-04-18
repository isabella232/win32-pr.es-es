---
title: Interfaz IWMPLibrary (VB y C) (WMP. h)
description: Representa una biblioteca. La interfaz IWMPLibrary expone las siguientes propiedades.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- IWMPLibrary (VB y C) interfaz de Windows Media Player
- IWMPLibrary (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPLibrary (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9749d3a2363c3863180639f249d7261ec1b9694
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690686"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Interfaz IWMPLibrary (VB y C#)

Representa una biblioteca.

La interfaz **IWMPLibrary** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPLibrary (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPLibrary (VB y C#)** tiene estos métodos.



| Método                                                                     | Descripción                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**isIdentical**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Devuelve un valor que indica si el objeto proporcionado es igual que el actual.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPLibrary (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso          | Descripción                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene una interfaz **IWMPMediaCollection** para la biblioteca actual.<br/> |
| [**name**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Solo lectura<br/> | Obtiene el nombre para mostrar de la biblioteca actual.<br/>                      |
| [**automáticamente**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Solo lectura<br/> | Obtiene un valor que indica el tipo de biblioteca.<br/>                      |



 

Obtenga una interfaz **IWMPLibrary** mediante el método siguiente.



| Object                                                   | Propiedad                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md) | [**getLibraryByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPLibraryServices. getLibraryByType (VB y C#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





