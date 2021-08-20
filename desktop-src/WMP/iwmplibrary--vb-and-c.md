---
title: Interfaz IWMPLibrary (VB y C) (Wmp.h)
description: Representa una biblioteca. La interfaz IWMPLibrary expone las siguientes propiedades.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- Interfaz IWMPLibrary (VB y C) Reproductor de Windows Media
- Interfaz IWMPLibrary (VB y C) Reproductor de Windows Media , descrita
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
ms.openlocfilehash: 6a418192e45363b6757d7360e779b8f8134677d8a321228d81fddd3d49501075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054833"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Interfaz IWMPLibrary (VB y C#)

Representa una biblioteca.

La **interfaz IWMPLibrary** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPLibrary (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPLibrary (VB y C#)** tiene estos métodos.



| Método                                                                     | Descripción                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**isIdentical**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Devuelve un valor que indica si el objeto proporcionado es el mismo que el actual.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPLibrary (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso          | Descripción                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene una **interfaz IWMPMediaCollection** para la biblioteca actual.<br/> |
| [**Nombre**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Solo lectura<br/> | Obtiene el nombre para mostrar de la biblioteca actual.<br/>                      |
| [**tipo**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Solo lectura<br/> | Obtiene un valor que indica el tipo de biblioteca.<br/>                      |



 

Obtenga una **interfaz IWMPLibrary** mediante el método siguiente.



| Object                                                   | Propiedad                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md) | [**getLibraryByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPLibraryServices.getLibraryByType (VB y C#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





