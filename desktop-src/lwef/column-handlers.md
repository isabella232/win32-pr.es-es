---
title: Crear controladores de columna
description: La vista Detalles del Explorador Windows Windows normalmente muestra varias columnas estándar.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- controladores de columnas
- register,column handlers
- Getcolumninfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90876aecdb2626326513723f0cd2c5a6e8f66bfd938b3f56cf10bd3624dd8687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349474"
---
# <a name="creating-column-handlers"></a>Crear controladores de columna

\[Esta característica solo se admite en Windows XP o versiones anteriores. \]

La vista Detalles del Explorador Windows Windows normalmente muestra varias columnas estándar. Cada columna muestra información, como el tamaño o el tipo de archivo, para cada archivo de la carpeta actual. Al implementar y registrar un controlador de columnas, puede hacer que las columnas personalizadas estén disponibles para su presentación.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Creación de controladores de extensión de shell](/windows/desktop/shell/handlers). Este documento se centra en los aspectos de implementación específicos de los controladores de columnas.

Se tratan los temas siguientes.

-   [Cómo funcionan los controladores de columnas](#how-column-handlers-work)
-   [Registrar controladores de columnas](#registering-column-handlers)
-   [Implementar controladores de columnas](#implementing-column-handlers)
    -   [Método Initialize](#the-initialize-method)
    -   [Método GetColumnInfo](#the-getcolumninfo-method)
    -   [Método GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Cómo funcionan los controladores de columnas

En la ilustración siguiente se Windows explorador en la vista Detalles.

![captura de pantalla del Explorador de Windows en la vista de detalles](images/columnproviderhandler1.jpg)

Con Windows 2000, la carpeta también puede admitir varias columnas que, de forma predeterminada, no se muestran. El usuario puede mostrar columnas adicionales haciendo clic con el botón derecho en uno de los encabezados de columna y seleccionando **el comando Más...** en el menú. A continuación, aparece un cuadro de diálogo que muestra las columnas disponibles para la carpeta y permite al usuario seleccionar las columnas que se mostrarán. En la ilustración siguiente se muestra este cuadro de diálogo para el ejemplo anterior.

![captura de pantalla del Explorador de Windows con el cuadro de diálogo Elegir detalles mostrado](images/columnproviderhandler2.jpg)

Al crear un controlador de columnas, puede crear columnas personalizadas y agregarlas a esa lista. Por ejemplo, una colección de archivos que contienen música podría usar un controlador de columnas para mostrar columnas que enumeran el intérprete y la pieza que contiene cada archivo.

Un controlador de columnas es un objeto global al que se llama cada vez Windows Explorador muestra la vista Detalles. Sin embargo, los controladores de columnas se usan normalmente para mostrar columnas personalizadas solo para miembros de un tipo de [archivo determinado.](/windows/desktop/shell/fa-file-types) Antes de mostrar la vista Detalles, Windows Explorer consulta a todos los controladores de columnas registrados sus características de columna. Si el usuario ha seleccionado una de las columnas del controlador, Windows Explorer consulta al controlador los datos asociados. Cuando un controlador de columnas recibe una solicitud de datos, la proporciona si el archivo es miembro de su tipo admitido. De lo contrario, omite la solicitud devolviendo S \_ FALSE.

## <a name="registering-column-handlers"></a>Registrar controladores de columnas

Los controladores de columna se registran en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Cree una subclave **de ColumnHandlers** denominada con el formato de cadena del GUID del identificador de clase (CLSID) del controlador. Para obtener una explicación general sobre cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](/windows/desktop/shell/handlers). En el ejemplo siguiente se muestra cómo registrar un controlador de columnas.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementar controladores de columnas

Al igual que todos los controladores de extensión de Shell, los controladores de columnas son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Exportan la [**interfaz IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) además de [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Windows Explorer llama a los tres métodos exportados por [**IColumnProvider para**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) solicitar la información que necesita para mostrar la columna. El procedimiento utilizado por Windows Explorer es:

1.  Llame [**a IColumnProvider::Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para especificar la carpeta que está a punto de mostrarse.
2.  Llame [**a IColumnProvider::GetColumnInfo para**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) recuperar el identificador y las características de la columna.
3.  Si el usuario ha seleccionado la columna, llame a [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada archivo de la carpeta para recuperar los datos que pertenecen a la entrada de columna del archivo.

### <a name="the-initialize-method"></a>Método Initialize

Windows El explorador llama [**a IColumnProvider::Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para inicializar el controlador de columnas. El método tiene tres parámetros, pero actualmente solo se usa *wszFolder.* Se establece en la carpeta cuya vista Detalles está a punto de mostrarse. Almacene el nombre de la carpeta para su uso posterior e inicialice el objeto de controlador según sea necesario.

### <a name="the-getcolumninfo-method"></a>Método GetColumnInfo

Windows A continuación, el [**Explorador llama a IColumnProvider::GetColumnInfo para**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) solicitar el identificador y las características de la columna. Pasa un índice para la columna del *parámetro dwIndex.* Este índice es un valor arbitrario que se usa para enumerar columnas. Windows El explorador también pasa un puntero a una [**estructura SHCOLUMNINFO.**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) Esta estructura se usa para devolver el identificador y las características de la columna. **IColumnProvider::GetColumnInfo debe** asignar los valores adecuados a los miembros de la estructura y devolver.

Las columnas se identifican mediante su identificador de conjunto de propiedades OLE (FMTID) y un identificador de propiedad asociado (PID). El primer miembro de la estructura [**SHCOLUMNINFO,**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) **scid**, es un puntero a una [**estructura SHCOLUMNID**](/windows/desktop/shell/objects) que se usa para identificar la columna. Su **miembro fmtid** contiene el FMTID de la columna y su **miembro pid** contiene el PID de la columna. Por ejemplo, un par FMTID/PID estándar que se usa normalmente para identificar columnas es el PID de autor del conjunto de propiedades Información de resumen.

Si es posible, el controlador debe usar los FMTID y los PID existentes para identificar la columna que admite. Si usa una estructura [**SHCOLUMNID personalizada,**](/windows/desktop/shell/objects) la columna mostrará datos solo para los archivos admitidos por el controlador. Si la carpeta contiene otros archivos, sus entradas estarán en blanco. Si una carpeta contiene archivos de más de un tipo de archivo, el uso de valores FMTID/PID estándar podría hacer posible combinar datos de distintos tipos en la misma columna.

Establezca el **miembro vt** en el [**tipo VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) de los datos que desea mostrar en la columna. El tipo más usado es VT LPSTR, ya que la mayoría de las columnas \_ muestran sus datos como cadenas de caracteres. Los miembros restantes de la [**estructura SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) se usan para definir las características de la columna. Asigne valores según corresponda.

### <a name="the-getitemdata-method"></a>Método GetItemData

Si se ha seleccionado la columna del controlador de columnas, Windows Explorer llama a [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada archivo de la carpeta que se va a mostrar. El *parámetro pscid* es un puntero a una [**estructura SHCOLUMNID**](/windows/desktop/shell/objects) que identifica la columna. El *parámetro pscd* apunta a una [**estructura SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) que identifica el archivo determinado.

El *parámetro pvarData* devuelve los datos que se deben mostrar en la columna del controlador para el archivo especificado por *pscd*. Si el controlador de columnas admite ese archivo, asigne su valor de datos *a pvarData* y devuelva S \_ OK. Si el controlador de columnas no admite el archivo, devuelva S FALSE sin asignar \_ un valor a *pvarData*.

Muchas carpetas contendrán una serie de archivos que no son compatibles con ningún controlador de columna determinado. Para mejorar la eficacia, [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) debe comprobar primero el miembro **pwszExt** de la estructura a la que apunta *pscd*. Este miembro contiene la extensión de nombre de archivo. Si la extensión indica que el archivo no es miembro de un tipo de archivo admitido por el controlador, evite el procesamiento innecesario devolviendo inmediatamente S \_ FALSE.

 

 