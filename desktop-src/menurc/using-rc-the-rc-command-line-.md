---
title: Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]
description: Para iniciar RC, use el siguiente comando.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e560ebee4312dccc2463caf123f05a5ad9831cd293c9976350e6de7ee13cb64a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971924"
---
# <a name="using-rc-the-rc-command-line"></a>Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]

Para iniciar RC, use el siguiente comando.

**RC** \[ *opciones* \] *script-file*

El *parámetro script-file* especifica el nombre del archivo de definición de recursos que contiene los nombres, tipos, nombres de archivo y descripciones de los recursos que se compilarán.

RC puede generar archivos de recursos independientes para las aplicaciones que tienen recursos independientes del lenguaje y específicos del lenguaje. Los desarrolladores [](/windows/desktop/Intl/preparing-resources) pueden usar un archivo de configuración de recursos o establecer opciones de línea de comandos para seleccionar qué tipos de recursos y elementos son recursos no localizables del archivo independiente del lenguaje [(LN)](/windows/desktop/Intl/mui-resource-management) y cuáles son recursos localizables de archivos DE CSV específicos del lenguaje. Para obtener más información, vea el [Interfaz de usuario multilingüe](/windows/desktop/Intl/multilingual-user-interface).

El *parámetro options* puede ser una o varias de las siguientes opciones de línea de comandos.

## <a name="options"></a>Opciones

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Muestra una lista de opciones de línea de comandos.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Define una página de códigos utilizada por la conversión nls.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Define un símbolo para el preprocesador que puede probar con la [**\# directiva ifdef.**](-ifdef.md)

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*
</dt> <dd>

RC crea un lenguaje neutro. Archivo RES y un archivo dependiente del lenguaje (MUI). Archivo RES mediante *script-file*. Esta opción debe usarse junto con **la opción /fo** *resname.* RC denomina al idioma neutro. El archivo RES *resname.res y* nombra al dependiente del lenguaje (MUI). Archivo RES *mresname.res*.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las [**funciones LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC crea un . Archivo RES denominado *resname mediante* *script-file*.

Si también se establece la opción **/fm** *mresname,* RC crea un idioma neutro. Archivo RES y un archivo dependiente del lenguaje (MUI). Archivo RES.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las [**funciones LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/g1**
</dt> <dd>

Si se establece /g1, RC genera un archivo CSV si el único recurso localizable que se incluye en el archivo DEA es un recurso de versión. Si no se establece /g1, RC no generará un archivo CSV si el único recurso localizable que se va a incluir en el archivo CSV es un recurso de versión.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Muestra la lista de opciones de línea de comandos.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Busca en el directorio especificado antes de buscar en los directorios especificados por la variable de entorno INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

Los tipos de recursos localizables RC se coloca en el elemento dependiente del lenguaje (MUI). Archivo RES. Si también se establece la opción **/q,** esta opción se omite y la información del archivo de configuración RC tiene prioridad.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las [**funciones LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *sobretipo*
</dt> <dd>

Tipos de recursos superpuestos que RC coloca en el idioma neutro. RES y el lenguaje dependiente (MUI). Archivos RES. Los tipos de recursos especificados por la opción **/k** deben ser un subconjunto de los especificados por la **opción /j.** Por ejemplo, ? J2 ? J3 ? K3 especifica que RC coloca el tipo de recurso 3 en los archivos neutrales del lenguaje y dependientes del lenguaje (MUI). Si también se establece la opción **/q,** esta opción se omite y la información del archivo de configuración RC tiene prioridad.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las [**funciones LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

Especifica el idioma predeterminado para la compilación. Por ejemplo, -l409 equivale a incluir la siguiente instrucción en la parte superior del archivo de script de recursos: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Para obtener más información, vea [Identificadores de lenguaje](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null finaliza todas las cadenas de la tabla de cadenas.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*
</dt> <dd>

Un archivo de configuración RC que sigue el formato de archivo de configuración rc. El formato de archivo de configuración RC permite que los componentes describan de forma automática la información de los recursos, como el control de versiones de recursos, la ruta de acceso del archivo DE LAN, los tipos de recursos y los elementos. Este archivo especifica qué recursos van al idioma neutro. Archivo RES y qué recursos van al archivo dependiente del lenguaje (CSV). Archivo RES. Esta opción y la información proporcionada en el archivo de configuración rc invalidan las opciones de línea de comandos **/j** **y /k**.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las [**funciones LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

ignorado. Se proporciona para la compatibilidad con los archivos Make existentes.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Desenlaza un símbolo para el preprocesador.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Muestra mensajes que informan sobre el progreso del compilador.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impide que RC comprueba la variable de entorno INCLUDE al buscar archivos de encabezado o archivos de recursos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las opciones no distinguen mayúsculas de minúsculas y se puede usar un guion (-) en lugar de una barra diagonal (/). Puede combinar opciones de una sola letra si no requieren parámetros adicionales.

RC no generará un archivo CSV en los siguientes casos.

-   No existen recursos localizables en el archivo .rc.
-   El único identificador de idioma de recurso especificado en el archivo .rc es neutro (0x0).
-   El archivo .rc tiene recursos que se especifican en más de un idioma. La excepción es si el archivo .rc contiene dos idiomas y un idioma es neutro (0x0), RC genera un archivo CSV.

Para obtener más información, vea los temas siguientes:

-   [Definir nombres para el preprocesador](defining-names-for-the-preprocessor.md)
-   [Cambiar el nombre del archivo de recursos compilado](renaming-the-compiled-resource-file.md)
-   [Búsqueda de archivos](searching-for-files.md)
-   [Mostrar mensajes de progreso](displaying-progress-messages.md)
-   [Mensajes de diagnóstico rc](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz de usuario multilingüe](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 