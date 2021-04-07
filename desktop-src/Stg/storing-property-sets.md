---
title: Almacenar conjuntos de propiedades
description: Las aplicaciones pueden exponer algunos de los datos de estado de sus documentos para que otras aplicaciones puedan buscar y leer esos datos.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Almacenar conjuntos de propiedades almacenamiento estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903200"
---
# <a name="storing-property-sets"></a>Almacenar conjuntos de propiedades

Las aplicaciones pueden exponer algunos de los datos de estado de sus documentos para que otras aplicaciones puedan buscar y leer esos datos. Algunos ejemplos son un conjunto de propiedades que describen el autor, el título y las palabras clave de un documento creado con un procesador de textos, o la lista de fuentes utilizadas en un documento. Esta instalación no está restringida a los documentos; también se puede utilizar en objetos incrustados. Por lo general, el acceso a los conjuntos de propiedades debe realizarse a través de las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , pero en esta sección se describe el método recomendado previamente.

> [!Note]  
> Si almacena un conjunto de propiedades que es interno de la aplicación, es posible que no desee usar las siguientes directrices. Para exponer la propiedad establecida en otras aplicaciones, siga estas instrucciones.

 

**Para almacenar un conjunto de propiedades en un archivo compuesto**

1.  Cree una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el mismo nivel de la estructura de almacenamiento que sus flujos de datos. Siga el nombre de la instancia de **IStorage** o **IStream** con " \\ 005". Los nombres de flujo y almacenamiento que comienzan por 0x05 se reservan para los conjuntos de propiedades comunes que se pueden compartir entre las aplicaciones. Además, las secuencias que comienzan con ese valor se limitan a 256 KB. Los nombres pueden seleccionarse desde nombres y formatos publicados, o bien asignando la propiedad set a FMTID y derivando el nombre de FMTID según las convenciones descritas en [convenciones de nomenclatura de objetos de almacenamiento](storage-object-naming-conventions.md).
2.  Un conjunto de propiedades se puede almacenar en una única instancia de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o en una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contenga varias secuencias y almacenamientos. En el caso de una instancia de **IStorage** , el flujo contenido denominado Contents es el flujo principal que contiene los valores de propiedad, donde algunos valores pueden ser nombres de otras secuencias o instancias de almacenamiento en el almacenamiento de este conjunto de propiedades.
3.  Especifique el CLSID de la clase de objeto que puede mostrar o proporcionar acceso mediante programación a los valores de propiedad. Si no hay ninguna clase de este tipo, el CLSID debe establecerse en el identificador de formato del conjunto de propiedades. En el caso de un conjunto de propiedades que use una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , establezca el CLSID de la instancia de **IStorage** para que sea el mismo que el almacenado en el flujo de contenido o en **CLSID \_ null**; el valor de una instancia de **IStorage** recién creada.
4.  Tiene la opción de especificar nombres que se puede mostrar que conforman el contenido del diccionario.

Algunas aplicaciones pueden leer solo las implementaciones de conjuntos de propiedades almacenadas como instancias de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) . Las aplicaciones se deben escribir para esperar que un conjunto de propiedades se pueda almacenar en una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o **IStream** , a menos que la definición del conjunto de propiedades indique lo contrario. Por ejemplo, la definición del conjunto de propiedades información de Resumen indica que solo se puede almacenar en una instancia de **IStream** con nombre. En los casos en los que se busca un conjunto de propiedades y no se sabe si se trata de un almacenamiento o una secuencia, busque una instancia de **IStream** con el nombre del conjunto de propiedades en primer lugar. Si se produce un error, busque una instancia de **IStorage** .

Para comprender mejor el almacenamiento de conjuntos de propiedades en una implementación de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , supongamos que hay una clase de aplicaciones que editan información sobre animales. En primer lugar, se define un CLSID (CLSID \_ AnimalApp) para este conjunto de aplicaciones, por lo que pueden indicar que comprenden conjuntos de propiedades que contienen información de los animales (**FMTID \_ AnimalInfo**) y otros que contienen información médica (**FMTID \_ MedicalInfo**).

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

Tenga en cuenta que el CLSID de la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y ambos conjuntos de propiedades es **CLSID \_ AnimalApp**. Esto identifica cualquier aplicación que pueda mostrar y/o proporcionar acceso mediante programación a estos conjuntos de propiedades. Cualquier aplicación puede leer los datos de los conjuntos de propiedades (los conjuntos de propiedades de punto detrás), pero solo las aplicaciones identificadas con el identificador de clase de CLSID \_ AnimalApp pueden entender el significado de los datos en los conjuntos de propiedades.

 

 




