---
description: Proporciona una plantilla para crear generadores de clases.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Clase CFactoryTemplate (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660845"
---
# <a name="cfactorytemplate-class"></a>Clase CFactoryTemplate

Proporciona una plantilla para crear generadores de clases.

En DirectShow, los generadores de clases se especializan mediante la clase **CFactoryTemplate** , también denominada *plantilla de fábrica*. Cada generador de clases contiene un puntero a una plantilla de fábrica. La plantilla de generador contiene información sobre un objeto COM, incluido el identificador de clase (CLSID) del objeto y un puntero a una función que crea el objeto.

En el archivo DLL, declare una matriz global de plantillas de fábrica denominada *g \_ templates*. Incluya una plantilla de generador para cada objeto en el archivo DLL. Cuando la función [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuevo generador de clases, busca en la matriz una plantilla con un CLSID coincidente. Suponiendo que encuentra una, crea un generador de clases que contiene un puntero a la plantilla coincidente. Cuando el cliente llama a **IClassFactory:: CreateInstance**, el generador de clases llama a la función de creación de instancias definida en la plantilla.

Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).



| Variables de miembro público                                                   | Descripción                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_nombre m**](cfactorytemplate-m-name.md)                                | Nombre del filtro.                                                        |
| [**ClsID de m \_**](cfactorytemplate-m-clsid.md)                              | Puntero al CLSID del objeto.                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | Puntero a una función que crea una instancia del objeto.              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | Puntero a una función a la que se llama desde el punto de entrada de DLL.           |
| [**\_filtro m pAMovieSetup \_**](cfactorytemplate-m-pamoviesetup-filter.md) | Puntero a una estructura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) . |
| Métodos públicos                                                            | Descripción                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Determina si un CLSID coincide con esta plantilla de clase.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Llama a la función de creación de objetos para la clase.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de clase base](base-class-reference.md)
</dt> </dl>

 

