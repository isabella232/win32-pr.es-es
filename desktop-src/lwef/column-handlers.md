---
title: Crear controladores de columnas
description: La vista de detalles del explorador de Windows de Windows muestra normalmente varias columnas estándar.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- Controladores de columnas
- registro, controladores de columnas
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940796e75f29ba0fcfa025d9a56267e14bdff38f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104562737"
---
# <a name="creating-column-handlers"></a>Crear controladores de columnas

\[Esta característica solo se admite en Windows XP o versiones anteriores. \]

La vista de detalles del explorador de Windows de Windows muestra normalmente varias columnas estándar. Cada columna muestra información, como el tipo o el tamaño del archivo, para cada archivo de la carpeta actual. Al implementar y registrar un controlador de columnas, puede hacer que las columnas personalizadas estén disponibles para su presentación.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](/windows/desktop/shell/handlers). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de columna.

Se tratan los temas siguientes.

-   [Cómo funcionan los controladores de columna](#how-column-handlers-work)
-   [Registrar controladores de columnas](#registering-column-handlers)
-   [Implementar controladores de columnas](#implementing-column-handlers)
    -   [Método Initialize](#the-initialize-method)
    -   [El método GetColumnInfo](#the-getcolumninfo-method)
    -   [El método GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Cómo funcionan los controladores de columna

En la ilustración siguiente se muestra el explorador de Windows en la vista detalles.

![captura de pantalla del explorador de Windows en la vista de detalles](images/columnproviderhandler1.jpg)

Con Windows 2000, la carpeta también puede admitir un número de columnas que, de forma predeterminada, no se muestran. El usuario puede mostrar columnas adicionales haciendo clic con el botón secundario en uno de los encabezados de columna y seleccionando el comando **más...** en el menú. Aparece un cuadro de diálogo que muestra las columnas disponibles para la carpeta y permite al usuario seleccionar las columnas que se van a mostrar. En la ilustración siguiente se muestra este cuadro de diálogo para el ejemplo anterior.

![captura de pantalla del explorador de Windows con el cuadro de diálogo elegir detalles mostrado](images/columnproviderhandler2.jpg)

Mediante la creación de un controlador de columnas, puede crear columnas personalizadas y agregarlas a esa lista. Por ejemplo, una colección de archivos que contienen música podría usar un controlador de columnas para mostrar las columnas que muestran el artista y el elemento que contiene cada archivo.

Un controlador de columnas es un objeto global al que se llama cada vez que el explorador de Windows muestra la vista de detalles. Sin embargo, los controladores de columnas se usan normalmente para mostrar las columnas personalizadas solo para los miembros de un [tipo de archivo](/windows/desktop/shell/fa-file-types)determinado. Antes de mostrar la vista de detalles, el explorador de Windows consulta todos los controladores de columna registrados para ver sus características de columna. Si el usuario ha seleccionado una de las columnas del controlador, el explorador de Windows consulta el controlador para los datos asociados. Cuando un controlador de columnas recibe una solicitud de datos, la proporciona si el archivo es miembro de su tipo admitido. De lo contrario, omite la solicitud devolviendo S \_ false.

## <a name="registering-column-handlers"></a>Registrar controladores de columnas

Los controladores de columnas se registran en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Cree una subclave de **ColumnHandlers** denominada con la forma de cadena del GUID del identificador de clase (CLSID) del controlador. Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](/windows/desktop/shell/handlers). En el ejemplo siguiente se muestra cómo registrar un controlador de columna.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementar controladores de columnas

Al igual que todos los controladores de extensión de Shell, los controladores de columna son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll. Exportan la interfaz [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) además de [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

El explorador de Windows llama a los tres métodos exportados por [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) para solicitar la información que necesita para mostrar la columna. El procedimiento utilizado por el explorador de Windows es:

1.  Llame a [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para especificar la carpeta que se va a mostrar.
2.  Llame a [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) para recuperar el identificador y las características de la columna.
3.  Si el usuario ha seleccionado la columna, llame a [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada archivo de la carpeta para recuperar los datos que pertenecen a la entrada de la columna del archivo.

### <a name="the-initialize-method"></a>Método Initialize

El explorador de Windows llama a [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para inicializar el controlador de columnas. El método tiene tres parámetros, pero actualmente solo se usa *wszFolder* . Se establece en la carpeta cuya vista de detalles está a punto de mostrarse. Almacene el nombre de la carpeta para su uso posterior e inicialice el objeto de controlador según sea necesario.

### <a name="the-getcolumninfo-method"></a>El método GetColumnInfo

El explorador de Windows siguiente llama a [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) para solicitar el identificador y las características de la columna. Pasa un índice para la columna en el parámetro *dwIndex* . Este índice es un valor arbitrario que se utiliza para enumerar columnas. El explorador de Windows también pasa un puntero a una estructura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) . Esta estructura se usa para devolver las características y el identificador de la columna. **IColumnProvider:: GetColumnInfo** debe asignar los valores adecuados a los miembros de la estructura y devolver.

Las columnas se identifican por su identificador de conjunto de propiedades OLE (FMTID) y un identificador de propiedad (PID) asociado. El primer miembro de la estructura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) , **SCID**, es un puntero a una estructura [**SHCOLUMNID**](/windows/desktop/shell/objects) que se utiliza para identificar la columna. Su miembro **fmtid** contiene el fmtid de la columna y su miembro **PID** contiene el PID de la columna. Por ejemplo, un par FMTID/PID estándar que se usa normalmente para identificar columnas es el PID de autor del conjunto de propiedades de información de resumen.

Si es posible, el controlador debe usar FMTIDs y PID existentes para identificar la columna que admite. Si usa una estructura [**SHCOLUMNID**](/windows/desktop/shell/objects) personalizada, la columna solo mostrará los datos de los archivos admitidos por el controlador. Si la carpeta contiene otros archivos, sus entradas estarán en blanco. Si una carpeta contiene archivos de más de un tipo de archivo, el uso de valores estándar de FMTID/PID podría permitir la combinación de datos de diferentes tipos en la misma columna.

Establezca el miembro **VT** en el tipo [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)   de los datos que desea mostrar en la columna. El tipo que se usa con más frecuencia es VT \_ LPSTR, ya que la mayoría de las columnas muestran sus datos como cadenas de caracteres. Los miembros restantes de la estructura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) se usan para definir las características de la columna. Asigne los valores según corresponda.

### <a name="the-getitemdata-method"></a>El método GetItemData

Si se ha seleccionado la columna del controlador de la columna, el explorador de Windows llama a [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada archivo de la carpeta que se va a mostrar. El parámetro *pscid* es un puntero a una estructura [**SHCOLUMNID**](/windows/desktop/shell/objects) que identifica la columna. El parámetro *PSCD* apunta a una estructura [**SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) que identifica el archivo determinado.

El parámetro *pvarData* devuelve los datos que se deben mostrar en la columna del controlador para el archivo especificado por *PSCD*. Si el controlador de columna admite ese archivo, asigne su valor de datos a *pvarData* y devuelva los valores \_ correctos. Si el archivo no es compatible con el controlador de columnas, devuelva S \_ false sin asignar un valor a *pvarData*.

Muchas carpetas contendrán una serie de archivos que no son compatibles con ningún controlador de columna determinado. Para mejorar la eficacia, [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) debe comprobar primero el miembro **pwszExt** de la estructura a la que apunta *PSCD*. Este miembro contiene la extensión de nombre de archivo. Si la extensión indica que el archivo no es un miembro de un tipo de archivo admitido por el controlador, evite el procesamiento innecesario devolviendo de inmediato S \_ false.

 

 