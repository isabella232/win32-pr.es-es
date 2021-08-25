---
description: Proporciona una plantilla para crear generadores de clases.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: CFactoryTemplate (clase, Combase.h)
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
ms.openlocfilehash: 1f9fbc76fe65e1f1136fb44d22db36500c4d8870f97befa8e36fa08a108ada71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697625"
---
# <a name="cfactorytemplate-class"></a>CFactoryTemplate (clase)

Proporciona una plantilla para crear generadores de clases.

En DirectShow, los generadores de clases se especializan mediante la **clase CFactoryTemplate,** también denominada plantilla *de generador*. Cada generador de clases contiene un puntero a una plantilla de generador. La plantilla de generador contiene información sobre un objeto COM, incluido el identificador de clase (CLSID) del objeto y un puntero a una función que crea el objeto.

En el archivo DLL, declare una matriz global de plantillas de generador denominada *g \_ Templates*. Incluya una plantilla de generador para cada objeto en el archivo DLL. Cuando la [**función DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuevo generador de clases, busca en la matriz una plantilla con un CLSID correspondiente. Suponiendo que encuentra uno, crea un generador de clases que contiene un puntero a la plantilla correspondiente. Cuando el cliente llama a **IClassFactory::CreateInstance**, el generador de clases llama a la función de creación de instancias definida en la plantilla.

Para obtener más información, [vea How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).



| Variables de miembro público                                                   | Descripción                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ Name**](cfactorytemplate-m-name.md)                                | Nombre del filtro.                                                        |
| [**m \_ ClsID**](cfactorytemplate-m-clsid.md)                              | Puntero al CLSID del objeto .                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | Puntero a una función que crea una instancia del objeto .              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | Puntero a una función a la que se llama desde el punto de entrada dll.           |
| [**m \_ pAMovieSetup \_ Filter**](cfactorytemplate-m-pamoviesetup-filter.md) | Puntero a una [**estructura FILTER \_ de AMOVIESETUP.**](amoviesetup-filter.md) |
| Métodos públicos                                                            | Descripción                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Determina si un CLSID coincide con esta plantilla de clase.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Llama a la función de creación de objetos para la clase .                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de clase base](base-class-reference.md)
</dt> </dl>

 

