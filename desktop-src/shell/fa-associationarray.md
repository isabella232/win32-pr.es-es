---
description: Una matriz de asociación es una lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo.
title: Matrices de asociación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154131"
---
# <a name="association-arrays"></a>Matrices de asociación

Una matriz de asociación es una lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo. El shell utiliza matrices de Asociación para consultar un conjunto predefinido de ubicaciones del registro que pueden contener información sobre un elemento de Shell.

Este tema se organiza de la siguiente manera:

-   [Acerca de las matrices de asociación](#about-association-arrays)
-   [Consultar matrices de asociación](#querying-association-arrays)
-   [Trabajar con matrices de Asociación para un origen de datos de Shell determinado](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Matrices de Asociación de orígenes de datos de Shell](#shell-data-source-association-arrays)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-association-arrays"></a>Acerca de las matrices de asociación

Una matriz de asociación es una lista ordenada de ubicaciones del registro que contienen información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo. Esta información sobre el tipo de elemento se puede registrar en distintos niveles de especificidad. Por ejemplo, puede registrar un verbo que se mostrará solo para un tipo de archivo específico (como. jpg) o para todos los elementos que tengan el mismo System. Kind (por ejemplo, System. Kind = Picture) o para todos los elementos.

El shell utiliza matrices de Asociación para consultar un conjunto predefinido de ubicaciones del registro que podrían contener información sobre el elemento. Las API de la matriz de asociación se pueden usar para recuperar de la subclave del registro un valor único que contiene la información solicitada, con ese valor procedente de la primera entrada de la matriz que lo proporciona. Por ejemplo, el valor del icono predeterminado se recupera de esta manera. La matriz de asociación también se puede utilizar para recuperar un conjunto de valores que se almacenan en las subclaves del registro. Por ejemplo, la lista de verbos se genera a partir de los verbos que se registran en todas las subclaves.

Una vez que el shell consulta un conjunto predefinido de ubicaciones del registro para obtener información sobre un elemento de Shell, coloca las ubicaciones del registro en una matriz en orden desde la ubicación más específica a la más general.

Dado que las matrices de asociación son listas ordenadas, proporcionan a los desarrolladores de aplicaciones un mecanismo para agregar información al registro que se devolverá para un tipo de elemento específico. Del mismo modo, las matrices de asociación permiten a los desarrolladores de aplicaciones agregar información al registro para un grupo específico de elementos cuando esos elementos se registran en una ubicación más general. Esta lógica informa de la decisión sobre la ubicación más adecuada en el registro para almacenar información sobre los elementos de Shell.

En un sistema Windows predeterminado, un archivo. jpg tiene la siguiente matriz de asociación:

-   **HKEY \_ Jpgfile \_ raíz de clases** \\ 
-   **HKEY \_ Clases \_ raíz** \\ **SystemFileAssociations** \\ **. jpg**
-   **HKEY \_ Imagen \_ raíz de clases** \\ 
-   **HKEY \_ \_raíz de clases** \\ * *\** _
-   _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects**

Para obtener información sobre cómo registrar matrices de asociación, vea [registro de aplicaciones](app-registration.md).

## <a name="querying-association-arrays"></a>Consultar matrices de asociación

Hay API de Shell para recuperar información de un intervalo de subclaves del registro, desde la subclave del registro más específica hasta un supraconjunto de la información en todas las subclaves del registro.

El uso más común de una matriz de asociación es consultar un valor único que el shell devuelve del elemento más específico de la matriz que tiene la información solicitada. En el ejemplo de código siguiente se muestra cómo hacerlo.


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



Las siguientes API se pueden usar para consultar una matriz de asociación o para construir un objeto de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de matriz de asociación que se pueda consultar:

-   [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (anterior a Windows Vista)
-   [**AssocCreateForClasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>Trabajar con matrices de Asociación para un origen de datos de Shell determinado

Cada origen de datos de Shell define la matriz de asociaciones para sus elementos. La definición de una matriz de asociación suele ser una función del tipo de elemento. Los implementadores de orígenes de datos de Shell deben definir y documentar las matrices de Asociación para permitir que las aplicaciones amplíen el comportamiento de esos tipos, como para registrar verbos u otra información. Las aplicaciones pueden extender el comportamiento de los elementos basándose en la adición de datos a las subclaves de la matriz de asociación, como agregar verbos para los elementos.

El origen de datos del sistema de archivos crea una matriz de asociaciones para los archivos basados en las siguientes subclaves del registro y ProgID especiales:

-   Si el archivo tiene un ProgID registrado, se utilizará el ProgID **\_ \_ raíz de las clases HKEY** \\  . En caso contrario, se usa **HKEY \_ classes \_ root** \\ **Unknown** .
-   La extensión de nombre de archivo se registra en **HKEY \_ classes \_ root** \\ **SystemFileAssociations** \\ *. fileExtension* subclave.
-   En la tabla siguiente se muestran los ProgID especiales. 

    | ProgID especial                                    | Descripción                   |
    |---------------------------------------------------|-------------------------------|
    | **HKEY \_ \_raíz de clases** \\ * *\** _                   | Todos los archivos (no carpetas)       |
    | _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects** | Archivos y carpetas del sistema de archivos |
    | **HKEY \_ Directorio \_ raíz de clases** \\             | Carpetas del sistema de archivos           |
    | **HKEY \_ Carpeta \_ raíz de clases** \\                | Contenedores de Shell              |

    

     

### <a name="shell-data-source-association-arrays"></a>Matrices de Asociación de orígenes de datos de Shell

La lista siguiente representa algunas de las matrices de asociación del almacén de datos de Shell que se pueden usar para los propósitos descritos en este tema:

-   **HKEY \_ \_raíz de clases** \\ * *\** _
-   _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects**
-   **HKEY \_Kind.Doc\_ raíz de clases** \\ **ument**
-   **HKEY \_ Resultados \_ raíz de clases** \\ 
-   **HKEY \_ Clases \_ raíz** \\ **SystemFileAssociations** \\ **. docx**
-   **HKEY \_ Clases \_ raíz** \\ **Word.Document. 12**

Las matrices de Asociación de orígenes de datos de Shell que se pueden usar para DBFolder (un almacén de datos de Shell que representa los elementos de los resultados de la búsqueda y las vistas basadas en consultas) son las siguientes:

-   Unidades
-   Red
-   RegItems
-   Ejemplos:
    -   ContentView
    -   Verbos

Otras matrices de asociaciones comunes incluyen carpetas e impresoras.

## <a name="additional-resources"></a>Recursos adicionales

-   Para crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](nse-implement.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> </dl>

 

 
