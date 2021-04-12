---
description: Preparación de un archivo de configuración de recursos
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparación de un archivo de configuración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154150"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparación de un archivo de configuración de recursos

Las utilidades del compilador MUIRCT y RC descritas en [Resource Utilities](resource-utilities.md) proporcionan una opción de línea de comandos que le permite especificar un archivo de configuración de recursos para los recursos de idioma base. El uso de este archivo XML público legible para el usuario permite un mayor control sobre la división de los recursos que se puede obtener mediante los modificadores de línea de comandos normales de las utilidades. Sin embargo, incluso si no proporciona un archivo de configuración de recursos como entrada, los archivos de recursos y específicos del idioma contendrán datos de configuración de recursos.

Todos los archivos de configuración de recursos para aplicaciones Win32 comienzan y finalizan de forma idéntica:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Este tema se centra en los aspectos del esquema XML que son útiles para compilar código no administrado en Windows Vista y versiones posteriores. En concreto, solo se ocupa del comportamiento del elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

El elemento win32Resources tiene los atributos que se describen en la tabla siguiente.



| Nombre del atributo           | Mandatory | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | No        | Tipo de archivo. Siempre debe ser "Application".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| suma de comprobación                 | No        | Valor de suma de comprobación que se va a mostrar en los datos de configuración de recursos del archivo LN y de los archivos de recursos específicos del lenguaje. Por ejemplo, este atributo le permite copiar la suma de comprobación de un solo archivo de recursos específico del idioma, por Convención la del inglés (Estados Unidos) y colocar la suma de comprobación en un archivo de recursos específico del lenguaje diferente. La suma de comprobación se puede especificar como una cadena de números hexadecimales que no tenga más de 32 caracteres. El valor numérico se debe poder contener en un número de 128 bits. |
| language                 | No        | Idioma especificado con un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | No        | Idioma que se va a insertar en los datos de configuración de recursos para el archivo LN, que representa el idioma de reserva final que se va a usar en una búsqueda de un archivo de recursos específico del idioma correspondiente. Si el cargador de recursos no puede cargar un archivo de recursos solicitado de los idiomas de interfaz de usuario preferidos del subproceso, utiliza un lenguaje de reserva final como último intento. El idioma se especifica con un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).       |
| ultimateFallbackLocation | No        | Ubicación de reserva. Especifique "Internal" si los recursos de reserva finales se compilan en el archivo LN. Especifique "external" (valor predeterminado) si el archivo LN va a hacer referencia a un archivo de recursos específico del idioma para sus recursos de reserva finales.                                                                                                                                                                                                                                                                                |



 

En el archivo de configuración de recursos, el elemento win32Resources tiene los subelementos descritos en la tabla siguiente.



| Nombre del elemento       | Descripción                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Recursos que encapsulan información sobre los tipos de recursos y los recursos individuales contenidos en un archivo de recursos específico del lenguaje. |
| neutralResources   | Recursos que encapsulan información sobre los tipos de recursos incluidos en un archivo LN.                                                 |



 

## <a name="localizedresources-element"></a>Elemento localizedResources

Elemento Resources adaptado. De forma predeterminada, este elemento no tiene atributos y solo un tipo de subelemento. Es simplemente un contenedor para los elementos resourceType.



| Nombre del atributo | Descripción                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Tipo de un recurso individual incluido en un archivo de recursos específico del lenguaje. |



 

## <a name="neutralresources-element"></a>Elemento neutralResources

Elemento de recursos neutros. Este elemento es simplemente un contenedor para los elementos resourceType.



| Nombre del atributo | Descripción                                        |
|----------------|----------------------------------------------------|
| resourceType   | Tipo de un único recurso incluido en un archivo LN. |



 

## <a name="resourcetype-element"></a>resourceType (elemento)

El elemento resourceType encapsula información sobre un único tipo de recurso o un recurso individual. Tiene los atributos que se enumeran a continuación.

> [!Caution]  
> Algunos defectos de configuración de recursos solo los detecta el compilador RC o MUIRCT, según el archivo de recursos de entrada o el contenido del archivo binario. No se detectan los errores resourceType del archivo de configuración de recursos que no existen en el archivo de entrada, lo que produce un comportamiento inesperado. Los usuarios pueden usar un archivo de configuración de recursos defectuoso y no saben hasta que introducen archivos binarios que usan las partes rotas del archivo de configuración de recursos, lo que crea la apariencia de que los saltos provienen de los archivos binarios actuales.

 



| Nombre del atributo | Mandatory | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Sí       | Nombre del tipo o identificador del recurso. Especifique un nombre de cadena o un número. Si usa un número, anteponga a la cadena un " \# " para indicar que representa un número. Cada elemento resourceType solo debe tener un atributo *typeNameId* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | No        | Cadena de nombre de elemento para el recurso que se va a colocar en el archivo de recursos específico del idioma. Puede especificar varios nombres, separados por espacios en blanco, por ejemplo, "MOFDATA HTML".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | No        | Identificador del elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma. El elemento se puede especificar como un intervalo (por ejemplo, "1-12") o por identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | No        | Identificador de cadena del elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma. La cadena se puede especificar como un intervalo (por ejemplo, "1-12") o por identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4"). Este atributo permite la especificación de entradas de la tabla de cadenas localizable y no localizable. Debe usarse junto con el valor de *typeNameId* de "6", que denota un tipo de recurso de entrada de tabla de cadenas.<br/> Las cadenas se almacenan en bloques de 16 en una tabla de cadenas. Por ejemplo, las cadenas 0 a 15 se almacenan en un único bloque de elementos de recursos y se puede hacer referencia a ellas en el archivo de configuración de recursos como *Itemid* 1, o como *stringId* "0-15". Por ejemplo, si hay cinco cadenas localizables y tres cadenas no localizables, debe asignar los identificadores de cadena 0-4 para las cadenas localizables y los identificadores de cadena 16-18 para las cadenas no localizables. Si no organiza las cadenas de esta manera, los bloques de cadenas afectados se colocan en el archivo LN y en el archivo de recursos específico del lenguaje.<br/> |



 

Si especifica los atributos *itemname*, *Itemid* y/o *stringId* para un tipo de recurso determinado en el elemento localizedResource, solo se colocan en el archivo de recursos específico del idioma estos elementos o cadenas especificados para el tipo de recurso designado. Si se especifica un elemento resourceType sin ningún nombre de elemento explícito, identificador de elemento o identificador de cadena, todos los elementos del tipo de recurso especificado se colocan en el archivo de recursos específico del lenguaje. Los elementos o tipos que no se enumeran en ningún elemento localizedResource se colocan en el archivo LN.

A continuación se muestran los tipos de recursos estándar y sus identificadores numéricos:

-   CURSOR (1)
-   MAPA DE BITS (2)
-   ICONO (3)
-   MENÚ (4)
-   CUADRO DE DIÁLOGO (5)
-   CADENA (6)
-   FONTDIR (7)
-   FUENTE (8)
-   ACELERADORES (9)
-   RCDATA (10)
-   MESSAGETABLE (11)
-   CURSOR de grupo \_ (12)
-   Icono de grupo \_ (14)
-   VERSIÓN (16)
-   HTML (23)

## <a name="example"></a>Ejemplo


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a>Observaciones

Si incluye cualquier tipo de recurso de icono (3), cuadro de diálogo (5), cadena (6) o versión (16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources. Puede ver esto en el ejemplo anterior, donde el tipo de recurso 16 aparece en las secciones de recursos neutros y localizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preparación de recursos](preparing-resources.md)
</dt> </dl>

 

 




