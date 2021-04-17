---
description: La tabla MsiEmbeddedUI define una interfaz de usuario incrustada en el paquete de Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Tabla MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52846e88e2d8f3edb439aa6b4a49c99e252173f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105653137"
---
# <a name="msiembeddedui-table"></a>Tabla MsiEmbeddedUI

La tabla MsiEmbeddedUI define una interfaz de usuario incrustada en el paquete de Windows Installer.

**[Windows Installer 4,0 o una versión anterior](not-supported-in-windows-installer-4-0.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 4,5.

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

La clave principal de la tabla.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre del archivo que recibe la información binaria en la columna de datos. El nombre del archivo es necesario para incluir una extensión. Por ejemplo, el nombre *embeddedui.dll* es aceptable, pero *embeddedui* es inaceptable. El nombre se puede localizar. Este campo puede contener un nombre de archivo corto o un nombre de archivo largo, pero no puede contener ambos. El formato de este campo es como el tipo de datos de la columna [filename](filename.md) , salvo que el separador de barra vertical ( \| ) para la sintaxis de nombre de archivo corto/nombre largo de archivo no está disponible. Dado que algunos servidores Web pueden distinguir mayúsculas de minúsculas, FileName debe coincidir exactamente con las mayúsculas y minúsculas de los archivos de origen para garantizar la compatibilidad con las descargas de Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Información sobre los datos de la columna de datos. El valor de este campo puede contener una o varias de las siguientes constantes.



| Constante                      | Hexadecimal | Decimal | Significado                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ninguno                          | 0x00        | 0       | El archivo no es el archivo DLL de la interfaz de usuario. Puede ser un archivo de recursos usado por la interfaz de usuario.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | El archivo DLL principal de la interfaz de usuario. No se puede marcar más de una fila en la tabla con este atributo. Si hay varias filas marcadas con este atributo, es un error y no se puede garantizar qué DLL se usa. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Permite al instalador invocar la interfaz de usuario incrustada durante una instalación básica de nivel de interfaz de usuario. El instalador omite este atributo si no se combina con el atributo **msidbEmbeddedUI** .                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Especifica los tipos de mensajes que se envían a la DLL de la interfaz de usuario. Esta columna solo es relevante para las filas con el atributo **msidbEmbeddedUI** . Este campo debe ser null si una fila hace referencia a un archivo de recursos y el valor de Attributes es NULL. Si una fila hace referencia a un archivo DLL de la interfaz de usuario, el valor de esta columna no debe ser null.

El valor de esta columna puede ser una combinación de los valores siguientes. El instalador omite cualquier otro valor.



| Constante                           | Hexadecimal | Decimal   | Descripción                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Finalización prematura.                                                                                       |
| **\_error INSTALLLOGMODE**          | 0x00002     | 2         | Mensajes de error.                                                                                              |
| **ADVERTENCIA de INSTALLLOGMODE \_**        | 0x00004     | 4         | Mensajes de advertencia.                                                                                            |
| **\_usuario INSTALLLOGMODE**           | 0x00008     | 8         | Mensajes de usuario.                                                                                               |
| **información de INSTALLLOGMODE \_**           | 0x00010     | 16        | Mensajes de estado no registrados.                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | Archivos actualmente en uso.                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | Solicitudes de resolución de código fuente.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Mensajes de espacio en disco.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Mensajes de inicio de acción.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Mensajes de datos de acción.                                                                                        |
| **progreso de INSTALLLOGMODE \_**       | 0x00400     | 1024      | Mensajes de progreso.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2048      | Mensajes de inicialización de la interfaz de usuario.                                                                                  |
| **INSTALLLOGMODE \_ inicializar**     | 0x01000     | 4096      | Mensajes de inicio de la interfaz de usuario enviados cuando se inicia una instalación del producto.                                            |
| **\_Finalizar INSTALLLOGMODE**      | 0x02000     | 8192      | Mensajes de cierre de la interfaz de usuario enviados una vez finalizada la instalación del producto.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Mensajes enviados antes de mostrar el cuadro de diálogo de la interfaz de usuario.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | Archivos actualmente en uso.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | Comienza la instalación del producto. El mensaje contiene el NombreProducto y el ProductCode del producto.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | La instalación de finaliza el producto. El mensaje contiene los valores ProductName, ProductCode y Return del producto. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Esta columna contiene información binaria. Si el campo de atributo está marcado con el atributo **msidbEmbeddedUI** , la información de este campo debe ser un archivo dll. Si el campo de atributo no es el atributo **msidbEmbeddedUI** , la información de este campo puede ser un archivo de recursos en cualquier formato.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar una interfaz de usuario incrustada, el desarrollador del programa de instalación debe crear esta funcionalidad en el paquete de Windows Installer. La tabla MsiEmbeddedUI define la interfaz de usuario incrustada. El archivo DLL de la interfaz de usuario incrustada debe exportar las funciones *InitializeEmbeddedUI*, *EmbeddedUIHandler* y *ShutdownEmbeddedUI* . Los paquetes que no admiten una interfaz de usuario incrustada pueden usar la interfaz de usuario interna de Windows Installer.

Para ejecutar [las herramientas de depuración para Windows](https://www.microsoft.com/?ref=go) en una interfaz de usuario incrustada, use las técnicas descritas en [depuración de acciones personalizadas](debugging-custom-actions.md). Establezca el valor de MsiBreak en MsiEmbeddedUI.

Para obtener un ejemplo de una interfaz de usuario personalizada incrustada, vea [usar una interfaz de usuario incrustada](using-an-embedded-ui.md).

 

 



