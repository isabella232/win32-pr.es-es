---
description: La tabla MsiEmbeddedUI define una interfaz de usuario insertada en el paquete Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Tabla MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7357a0b5aa1de2218eefb58fa85fbe374e9796ad0aaa94946743f1c51d9c8daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012953"
---
# <a name="msiembeddedui-table"></a>Tabla MsiEmbeddedUI

La tabla MsiEmbeddedUI define una interfaz de usuario insertada en el paquete Windows Installer.

**[Windows Instalador 4.0 o anterior:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 4.5.

La tabla MsiEmbeddedUI tiene las columnas siguientes.



| Columna        | Tipo                               | Clave | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identificador](identifier.md)       | Y   | N        |
| FileName      | [Texto](text.md)                   | N   | N        |
| Atributos    | [Entero](integer.md)             | N   | N        |
| MessageFilter | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Datos          | [Binario](binary.md)               | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

Clave principal de la tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Nombre del archivo que recibe la información binaria en la columna Datos. El nombre del archivo es necesario para incluir una extensión. Por ejemplo, el nombre *embeddedui.dll* es aceptable, pero *embeddedui* no es aceptable. El nombre se puede localizar. Este campo puede contener un nombre de archivo corto o un nombre de archivo largo, pero no puede contener ambos. El formato de este campo es similar al tipo de datos de columna [Nombre](filename.md) de archivo, salvo que el separador de barra vertical ( ) para la sintaxis de nombre de archivo corto o nombre de archivo \| largo no está disponible. Dado que algunos servidores web pueden distinguen mayúsculas de minúsculas, FileName debe coincidir exactamente con el caso de los archivos de origen para garantizar la compatibilidad con las descargas de Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Información sobre los datos de la columna Datos. El valor de este campo puede contener una o varias de las constantes siguientes.



| Constante                      | Hexadecimal | Decimal | Significado                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ninguno                          | 0x00        | 0       | El archivo no es el archivo DLL de la interfaz de usuario. Puede ser un archivo de recursos usado por la interfaz de usuario.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | Archivo DLL principal para la interfaz de usuario. No se puede marcar más de una fila de la tabla con este atributo. Si se marcan varias filas con este atributo, es un error y no se puede garantizar qué dll se usa. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Permite que el instalador invoque la interfaz de usuario incrustada durante una instalación de nivel de interfaz de usuario básica. El instalador omite este atributo si no se combina con el **atributo msidbEmbeddedUI.**                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Especifica los tipos de mensajes que se envían al archivo DLL de la interfaz de usuario. Esta columna solo es relevante para las filas con el **atributo msidbEmbeddedUI.** Este campo debe ser NULL si una fila hace referencia a un archivo de recursos y el valor de Attributes es NULL. Si una fila hace referencia a un archivo DLL de interfaz de usuario, el valor de esta columna no debe ser NULL.

El valor de esta columna puede ser una combinación de los valores siguientes. El instalador omite cualquier otro valor.



| Constante                           | Hexadecimal | Decimal   | Descripción                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Terminación prematura.                                                                                       |
| **INSTALLLOGMODE \_ ERROR**          | 0x00002     | 2         | Mensajes de error.                                                                                              |
| **ADVERTENCIA DE \_ INSTALLLOGMODE**        | 0x00004     | 4         | Mensajes de advertencia.                                                                                            |
| **INSTALLLOGMODE \_ USER**           | 0x00008     | 8         | Mensajes de usuario.                                                                                               |
| **INSTALLLOGMODE \_ INFO**           | 0x00010     | 16        | Mensajes de estado sin etiquetar.                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | Archivos que se mantienen actualmente en uso.                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | Solicitudes de resolución de origen.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Mensajes de espacio en disco.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Mensajes de inicio de acción.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Mensajes de datos de acción.                                                                                        |
| **PROGRESO DE \_ INSTALLLOGMODE**       | 0x00400     | 1024      | Mensajes de progreso.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2048      | Mensajes de inicialización de la interfaz de usuario.                                                                                  |
| **INSTALLLOGMODE \_ INITIALIZE**     | 0x01000     | 4096      | Mensajes de inicio de la interfaz de usuario enviados cuando se inicia la instalación de un producto.                                            |
| **INSTALLLOGMODE \_ TERMINATE**      | 0x02000     | 8192      | Mensajes de cierre de la interfaz de usuario enviados una vez finalizada la instalación de un producto.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Mensajes enviados antes de mostrar el cuadro de diálogo de interfaz de usuario.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | Archivos que se mantienen actualmente en uso.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | Comienza la instalación del producto. El mensaje contiene los valores ProductName y ProductCode del producto.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | La instalación del producto finaliza. El mensaje contiene los valores ProductName, ProductCode y return del producto. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Esta columna contiene información binaria. Si el campo Atributo está marcado con el atributo **msidbEmbeddedUI,** la información de este campo debe ser un archivo DLL. Si el campo Atributo no es **el atributo msidbEmbeddedUI,** la información de este campo puede ser un archivo de recursos en cualquier formato.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para usar una interfaz de usuario incrustada, el desarrollador del programa de instalación debe crear esta funcionalidad en el paquete Windows Installer. La tabla MsiEmbeddedUI define la interfaz de usuario insertada. El archivo DLL de la interfaz de usuario insertada debe exportar las funciones *InitializeEmbeddedUI*, *EmbeddedUIHandler* y *ShutdownEmbeddedUI.* Los paquetes que no admiten una interfaz de usuario insertadas pueden usar Windows interfaz de usuario interna del instalador.

Para ejecutar [Herramientas de depuración Windows](https://www.microsoft.com/?ref=go) en una interfaz de usuario insertadas, use las técnicas descritas en [Depuración de acciones personalizadas](debugging-custom-actions.md). Establezca el valor de MsiBreak en MsiEmbeddedUI.

Para obtener un ejemplo de una interfaz de usuario personalizada incrustada, [consulte Uso de una interfaz de usuario incrustada.](using-an-embedded-ui.md)

 

 



