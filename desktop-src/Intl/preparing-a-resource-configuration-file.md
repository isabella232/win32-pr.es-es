---
description: Preparar un archivo de configuración de recursos
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparar un archivo de configuración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063037"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparar un archivo de configuración de recursos

Las utilidades MUIRCT y RC [](resource-utilities.md) Compiler descritas en Utilidades de recursos proporcionan una opción de línea de comandos que permite especificar un archivo de configuración de recursos para los recursos del lenguaje base. El uso de este archivo XML público y legible permite tener más control sobre la división de recursos de lo que se puede obtener mediante los modificadores de línea de comandos normales de las utilidades. Sin embargo, aunque no proporcione un archivo de configuración de recursos como entrada, el LN y los archivos de recursos específicos del lenguaje contendrán datos de configuración de recursos.

Todos los archivos de configuración de recursos para aplicaciones Win32 comienzan y terminan de forma idéntica:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Este tema se centra en los aspectos del esquema XML que son útiles para compilar código no administrado en Windows Vista y versiones posteriores. En concreto, solo se refiere al comportamiento del elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

El elemento win32Resources tiene los atributos descritos en la tabla siguiente.



| Nombre del atributo           | Mandatory | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | No        | Tipo de archivo. Siempre debe ser "Aplicación".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| suma de comprobación                 | No        | Valor de suma de comprobación que aparece en los datos de configuración de recursos del archivo LN y los archivos de recursos específicos del lenguaje. Por ejemplo, este atributo permite copiar la suma de comprobación de un único archivo de recursos específico del idioma, por convención el de inglés (Estados Unidos) y colocar la suma de comprobación en un archivo de recursos específico del idioma diferente. La suma de comprobación se puede especificar como una cadena de número hexadecimal que no tenga más de 32 caracteres. El valor numérico debe ser contenido en un número de 128 bits. |
| language                 | No        | Idioma especificado mediante un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | No        | Idioma que se insertará en los datos de configuración de recursos del archivo LN, que representa el idioma de reserva final que se usará en una búsqueda de un archivo de recursos específico del idioma correspondiente. Si el cargador de recursos no puede cargar un archivo de recursos solicitado desde los idiomas de interfaz de usuario preferidos del subproceso, usa un idioma de reserva final como último intento. El idioma se especifica mediante un formato de nombre compatible con RFC 4646 (Windows Vista y versiones posteriores), por ejemplo, en-US para inglés (Estados Unidos).       |
| ultimateFallbackLocation | No        | Ubicación de reserva. Especifique "internal" si los recursos de reserva finales se compilan en el archivo LN. Especifique "external" (valor predeterminado) si el archivo LN hace referencia a un archivo de recursos específico del lenguaje para sus recursos de reserva finales.                                                                                                                                                                                                                                                                                |



 

En el archivo de configuración de recursos, el elemento win32Resources tiene los sub-elementos descritos en la tabla siguiente.



| Nombre del elemento       | Descripción                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Recursos que encapsulan información sobre los tipos de recursos y los recursos individuales contenidos en un archivo de recursos específico del lenguaje. |
| neutralResources   | Recursos que encapsulan información sobre los tipos de recursos contenidos en un archivo LN.                                                 |



 

## <a name="localizedresources-element"></a>elemento localizedResources

Elemento de recursos localizados. De forma predeterminada, este elemento no tiene atributos y solo un tipo de sub element. Es simplemente un contenedor para los elementos resourceType.



| Nombre del atributo | Descripción                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Tipo de un recurso individual contenido en un archivo de recursos específico del idioma. |



 

## <a name="neutralresources-element"></a>elemento neutralResources

Elemento recursos neutros. Este elemento es simplemente un contenedor para los elementos resourceType.



| Nombre del atributo | Descripción                                        |
|----------------|----------------------------------------------------|
| resourceType   | Tipo de un único recurso contenido en un archivo LN. |



 

## <a name="resourcetype-element"></a>elemento resourceType

El elemento resourceType encapsula información sobre un único tipo de recurso o recurso individual. Tiene los atributos que se enumeran a continuación.

> [!Caution]  
> Algunos defectos de configuración de recursos solo los detecta el compilador RC o MUIRCT, según el archivo de recursos de entrada o el contenido del archivo binario. Los errores resourceType del archivo de configuración de recursos que no existen en el archivo de entrada no se detectan, lo que produce un comportamiento inesperado. Los usuarios pueden usar un archivo de configuración de recursos defectuosos y no lo saben hasta que introducen archivos binarios que usan las partes rotas del archivo de configuración de recursos, lo que crea la apariencia de que las interrupciones son de los archivos binarios actuales.

 



| Nombre del atributo | Mandatory | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Sí       | Escriba el nombre o el identificador del recurso. Especifique un nombre de cadena o un número. Si usa un número, antepone la cadena con " \# " " para indicar que representa un número. Cada elemento resourceType solo debe tener un *atributo typeNameId.*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | No        | Cadena de nombre de elemento para el recurso que se va a colocar en el archivo de recursos específico del idioma. Puede especificar varios nombres, separados por espacios en blanco, por ejemplo, "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | No        | Identificador del elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma. El elemento se puede especificar como un intervalo (por ejemplo, "1-12") o mediante identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | No        | Identificador de cadena para un elemento de recurso individual que se va a colocar en el archivo de recursos específico del idioma. La cadena se puede especificar como un intervalo (por ejemplo, "1-12") o mediante identificadores individuales separados por espacios en blanco (por ejemplo, "1 3 4"). Este atributo permite especificar entradas de tabla de cadena localizables y no localizables. Debe usarse junto con el valor *typeNameId* de "6", lo que indica un tipo de recurso de entrada de tabla de cadenas.<br/> Las cadenas se almacenan en bloques de 16 en una tabla de cadenas. Por ejemplo, las cadenas de 0 a 15 se almacenan en un único bloque de elemento de recurso y se puede hacer referencia en el archivo de configuración de recursos como *itemId* 1 o *como stringId* "0-15". Por ejemplo, si hay cinco cadenas localizables y tres cadenas no localizables, debe asignar los identificadores de cadena 0-4 para las cadenas localizables y los identificadores de cadena 16-18 para las cadenas no localizables. Si no organiza las cadenas de esta manera, los bloques de cadenas afectados se colocan tanto en el archivo LN como en el archivo de recursos específico del idioma.<br/> |



 

Si especifica los atributos *itemName*, *itemId* o *stringId* para un tipo de recurso determinado en el elemento localizedResource, solo estos elementos o cadenas especificados para el tipo de recurso designado se colocan en el archivo de recursos específico del idioma. Si se especifica un elemento resourceType sin ningún nombre de elemento explícito, identificador de elemento o identificador de cadena, todos los elementos del tipo de recurso especificado se colocan en el archivo de recursos específico del idioma. Los elementos o tipos que no aparecen en ningún elemento localizedResource se colocan en el archivo LN.

Estos son los tipos de recursos estándar y sus identificadores numéricos:

-   CURSOR(1)
-   BITMAP(2)
-   ICON(3)
-   MENU(4)
-   DIALOG(5)
-   STRING(6)
-   FONTDIR(7)
-   FONT(8)
-   ACCELERATORS(9)
-   RCDATA(10)
-   MESSAGETABLE(11)
-   GROUP \_ CURSOR(12)
-   ICONO \_ DE GRUPO(14)
-   VERSION(16)
-   HTML(23)

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

Si incluye algún tipo de recurso ICON(3), DIALOG(5), STRING(6) o VERSION(16) en el elemento neutralResources, tendrá que duplicar esa entrada en el elemento localizedResources. Puede ver esto ilustrado en el ejemplo anterior, donde el tipo de recurso 16 aparece en las secciones recursos neutros y localizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preparación de recursos](preparing-resources.md)
</dt> </dl>

 

 




