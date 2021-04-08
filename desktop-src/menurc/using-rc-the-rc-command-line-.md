---
title: Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]
description: Para iniciar RC, use el siguiente comando.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995182"
---
# <a name="using-rc-the-rc-command-line"></a>Using RC (The RC Command Line) [Uso de RC (la línea de comandos de RC)]

Para iniciar RC, use el siguiente comando.

**RC** \[ *Opciones* \] de *archivo de script*

El parámetro *script-File* especifica el nombre del archivo de definición de recursos que contiene los nombres, tipos, nombres de archivo y descripciones de los recursos que se van a compilar.

RC puede generar archivos de recursos independientes para las aplicaciones que tienen recursos independientes del idioma y específicos del idioma. Los desarrolladores pueden usar un [archivo de configuración de recursos](/windows/desktop/Intl/preparing-resources) o establecer opciones de línea de comandos para seleccionar qué tipos de recursos y elementos son recursos no localizables del [archivo independiente del lenguaje (LN)](/windows/desktop/Intl/mui-resource-management) y cuáles son recursos localizables de archivos mui específicos del idioma. Para obtener más información, consulte la [interfaz de usuario multilingüe](/windows/desktop/Intl/multilingual-user-interface).

El parámetro *Options* puede ser una o varias de las siguientes opciones de la línea de comandos.

## <a name="options"></a>Opciones

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Muestra una lista de opciones de la línea de comandos.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Define una página de códigos que utiliza la conversión de NLS.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d.**
</dt> <dd>

Define un símbolo para el preprocesador que se puede probar con la directiva [**\# ifdef**](-ifdef.md) .

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*
</dt> <dd>

RC crea un independiente del idioma. Archivo RES y una dependiente del lenguaje (MUI). Archivo RES con *el archivo de script*. Esta opción debe usarse junto con la opción **/FO** *resname* . RC da nombre al idioma neutro. Archivo RES *resname. res* y el nombre depende del idioma (MUI). Archivo RES *mresname. res*.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *resname*
</dt> <dd>

RC crea un. Archivo RES denominado *resname* con *el archivo de script*.

Si también se establece la opción **/FM** *mresname* , RC crea un independiente del idioma. Archivo RES y una dependiente del lenguaje (MUI). Archivo RES.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/G1**
</dt> <dd>

Si se establece/G1, RC genera un archivo MUI si el único recurso traducible que se incluye en el archivo MUI es un recurso de versión. Si no se establece/G1, RC no generará un archivo MUI si el único recurso traducible que se incluye en el archivo MUI es un recurso de versión.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Muestra la lista de opciones de la línea de comandos.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Busca en el directorio especificado antes de buscar en los directorios especificados por la variable de entorno INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *LOCTYPE*
</dt> <dd>

Los tipos de recursos localizables RC colocan en el dependiente del lenguaje (MUI). Archivo RES. Si también se establece la opción **/q** , se omite esta opción y la información del archivo de configuración RC tiene prioridad.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** - *sobretype*
</dt> <dd>

Los tipos de recursos superpuestos que RC colocan en el lenguaje neutro. RES y el dependiente del lenguaje (MUI). Archivos RES. Los tipos de recursos especificados por la opción **/k** deben ser un subconjunto de los especificados por la opción **/j** . Por ejemplo,? J2? J3? K3 especifica que RC coloca el tipo de recurso 3 en los archivos independientes del idioma y del idioma (MUI). Si también se establece la opción **/q** , se omite esta opción y la información del archivo de configuración RC tiene prioridad.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

Especifica el idioma predeterminado para la compilación. Por ejemplo,-l409 es equivalente a incluir la siguiente instrucción en la parte superior del archivo de script de recursos: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Para obtener más información, vea [identificadores de idioma](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null finaliza todas las cadenas de la tabla de cadenas.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. RCConfig*
</dt> <dd>

Un archivo de configuración RC que sigue el formato del archivo de configuración RC. El formato de archivo de configuración RC permite a los componentes describir automáticamente la información de recursos, como el control de versiones de recursos, la ruta de acceso del archivo MUI, los tipos de recursos y los elementos. Este archivo especifica qué recursos entran en el idioma neutro. Archivo RES y los recursos que se incluyen en el lenguaje (MUI). Archivo RES. Esta opción y la información proporcionada en el archivo de configuración RC invalidan las opciones de línea de comandos **/j** y **/k**.

**Windows Server 2003 y Windows XP/2000:** Esta opción no está disponible sin usar también las funciones [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) en un sistema actualizado.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

ignorado. Se proporciona para ofrecer compatibilidad con los archivos make existentes.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Anula la definición de un símbolo para el preprocesador.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Muestra mensajes que informan sobre el progreso del compilador.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impide que RC Compruebe la variable de entorno INCLUDE al buscar archivos de encabezado o archivos de recursos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las opciones no distinguen mayúsculas de minúsculas y se puede usar un guion (-) en lugar de una barra diagonal (/). Puede combinar las opciones de una sola letra si no requieren ningún parámetro adicional.

RC no generará un archivo MUI en los casos siguientes.

-   No existe ningún recurso traducible en el archivo. rc.
-   El único identificador de idioma de recurso especificado en el archivo. RC es neutro (0X0).
-   El archivo. rc tiene recursos que se especifican en más de un idioma. La excepción es si el archivo. RC contiene dos idiomas y un idioma es neutro (0X0), RC genera un archivo MUI.

Para obtener más información, vea los temas siguientes:

-   [Definir nombres para el preprocesador](defining-names-for-the-preprocessor.md)
-   [Cambiar el nombre del archivo de recursos compilados](renaming-the-compiled-resource-file.md)
-   [Buscar archivos](searching-for-files.md)
-   [Mostrar mensajes de progreso](displaying-progress-messages.md)
-   [RC mensajes de diagnóstico](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz de usuario multilingüe](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 