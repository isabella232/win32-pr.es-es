---
title: Clave CLSID
description: Un CLSID es un identificador único global que identifica un objeto de clase COM. Si el servidor o el contenedor permiten la vinculación a los objetos incrustados, debe registrar un CLSID para cada clase admitida de objetos.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- Clave del registro CLSID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9253446a039e47996366c7dfdb51c01f9b1993
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418931"
---
# <a name="clsid-key"></a>Clave CLSID

Un CLSID es un identificador único global que identifica un objeto de clase COM. Si el servidor o el contenedor permiten la vinculación a los objetos incrustados, debe registrar un CLSID para cada clase admitida de objetos.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_Clases de software de máquina local \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Clave del Registro                                                 | Descripción                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | Asocia un AppID a un CLSID.                                                                                                        |
| [**Conversión a**](autoconvertto.md)                       | Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos.                                                |
| [**Autotreatas**](autotreatas.md)                           | Establece automáticamente el CLSID para la clave [**treatAs**](treatas.md) en el valor especificado.                                              |
| [**AuxUserType**](auxusertype.md)                           | Especifica el nombre para mostrar corto y los nombres de aplicación de una aplicación.                                                                     |
| [**Control**](control.md)                                   | Identifica un objeto como un control ActiveX.                                                                                              |
| [**Conversión**](conversion.md)                             | Lo utiliza el cuadro de diálogo **convertir** para determinar los formatos que una aplicación puede leer y escribir.                                           |
| [**DataFormats**](dataformats.md)                           | Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Proporciona información de icono predeterminada para presentaciones con iconos de objetos.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Especifica si una aplicación utiliza un controlador personalizado.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Especifica si una aplicación utiliza un controlador personalizado.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Especifica la ruta de acceso al archivo DLL de servidor en proceso.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.                           |
| [**Insertable**](insertable.md)                             | Indica que los objetos de esta clase deben aparecer en el cuadro de lista del cuadro de diálogo **Insertar objeto** cuando lo usan las aplicaciones de contenedor com. |
| [**Interfaz**](interface.md)                               | Una entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.                                             |
| [**LocalServer**](localserver.md)                           | Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Especifica cómo crear y mostrar un objeto.                                                                                           |
| [**ProgID**](progid.md)                                     | Asocia un ProgID a un CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 x 16 que se va a usar para el aspecto de una barra de herramientas o un botón del cuadro de herramientas.                      |
| [**Tratar**](treatas.md)                                   | Especifica el CLSID de una clase que puede emular la clase actual.                                                                       |
| [**Verbo**](verb.md)                                         | Especifica los verbos que se van a registrar para una aplicación.                                                                                 |
| [**Versión**](version.md)                                   | Especifica el número de versión del control.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Asocia un ProgID a un CLSID. Este valor se usa para determinar la versión más reciente de una aplicación de objeto.                           |



 

## <a name="remarks"></a>Observaciones

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

La clave CLSID contiene información utilizada por el controlador COM predeterminado para devolver información sobre una clase cuando está en estado de ejecución.

Para obtener un CLSID para la aplicación, puede usar el Uuidgen.exe o usar la función [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .

El CLSID es un número de 128 bits, en hexadecimal, dentro de un par de llaves.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




