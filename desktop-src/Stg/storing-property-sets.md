---
title: Almacenar conjuntos de propiedades
description: Las aplicaciones pueden exponer algunos de los datos de estado de sus documentos para que otras aplicaciones puedan buscar y leer esos datos.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Almacenar conjuntos de propiedades estructurados Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beae3d03889415fd920cb34d065c0ffd33e813b170d45dd73ae7c4d548f9296d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661785"
---
# <a name="storing-property-sets"></a>Almacenar conjuntos de propiedades

Las aplicaciones pueden exponer algunos de los datos de estado de sus documentos para que otras aplicaciones puedan buscar y leer esos datos. Algunos ejemplos son un conjunto de propiedades que describe el autor, el título y las palabras clave de un documento creado con un procesador de palabras o la lista de fuentes usadas en un documento. Esta instalación no está restringida a los documentos; también se puede usar en objetos incrustados. Por lo general, el acceso a los conjuntos de propiedades debe realizarse a través de las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pero en esta sección se describe la manera recomendada anteriormente.

> [!Note]  
> Si almacena un conjunto de propiedades que es interno de la aplicación, es posible que no desee usar las siguientes directrices. Para exponer el conjunto de propiedades a otras aplicaciones, siga estas instrucciones.

 

**Para almacenar un conjunto de propiedades en un archivo compuesto**

1.  Cree una [**instancia de IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**o IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el mismo nivel de la estructura de almacenamiento que sus flujos de datos. Siga el nombre de la **instancia de IStorage** **o IStream** con \\ "005". Los nombres de flujo y almacenamiento que comienzan por 0x05 están reservados para conjuntos de propiedades comunes que se pueden compartir entre las aplicaciones. Además, las secuencias que comienzan con ese valor están limitadas a 256 KB. Los nombres se pueden seleccionar de nombres y formatos publicados, o asignando el conjunto de propiedades un FMTID y derivando el nombre del FMTID según las convenciones descritas en [Storage Convenciones](storage-object-naming-conventions.md)de nomenclatura de objetos .
2.  Un conjunto de propiedades se puede almacenar en una única [**instancia de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o en una [**instancia de IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contiene varios flujos y almacenamientos. En el caso de una instancia de **IStorage,** la secuencia independiente denominada Contents es la secuencia principal que contiene valores de propiedad, donde algunos valores pueden ser nombres de otras secuencias o instancias de almacenamiento dentro del almacenamiento para este conjunto de propiedades.
3.  Especifique el CLSID de la clase de objeto que puede mostrar o proporcionar acceso mediante programación a los valores de propiedad. Si no hay ninguna clase de este tipo, el CLSID debe establecerse en el identificador de formato del conjunto de propiedades. Para un conjunto de propiedades que usa una instancia de [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) establezca el CLSID de la instancia de **IStorage** para que sea el mismo que el almacenado en la secuencia Contents o en **CLSID \_ NULL**; el valor de una instancia de **IStorage** recién creada.
4.  Tiene la opción de especificar nombres que se pueden mostrar que forman el contenido del diccionario.

Algunas aplicaciones pueden leer solo implementaciones de conjuntos de propiedades almacenados como [**instancias de IStream.**](/windows/desktop/api/Objidl/nn-objidl-istream) Las aplicaciones deben escribirse para esperar que un conjunto de propiedades se pueda almacenar en una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o **IStream,** a menos que la definición del conjunto de propiedades indique lo contrario. Por ejemplo, la definición del conjunto de propiedades Información de resumen indica que solo se puede almacenar en una instancia **IStream** con nombre. En los casos en los que busque un conjunto de propiedades y no sepa si es un almacenamiento o una secuencia, busque primero una instancia **de IStream** con el nombre del conjunto de propiedades. Si se produce un error, busque una **instancia de IStorage.**

Para comprender mejor el almacenamiento de conjuntos de propiedades en una implementación [**de IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) suponga que hay una clase de aplicaciones que editan información sobre animales. En primer lugar, se define un CLSID (CLSID ZooApp) para este conjunto de aplicaciones, por lo que pueden indicar que entienden los conjuntos de propiedades que contienen información \_ de animales **(FMTID \_ ZooInfo)** y otros que contienen información médica **(FMTID \_ MedicalInfo).**

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

Tenga en cuenta que el CLSID de la [**interfaz IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y ambos conjuntos de propiedades **es CLSID \_ ZooApp**. Esto identifica cualquier aplicación que pueda mostrar o proporcionar acceso mediante programación a estos conjuntos de propiedades. Cualquier aplicación puede leer los datos dentro de los conjuntos de propiedades (el punto detrás de los conjuntos de propiedades), pero solo las aplicaciones identificadas con el identificador de clase de CLSID ZooApp pueden comprender el significado de los datos en los conjuntos de \_ propiedades.

 

 




