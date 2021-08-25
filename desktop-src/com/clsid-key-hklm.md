---
title: Clave CLSID
description: Un CLSID es un identificador único global que identifica un objeto de clase COM. Si el servidor o contenedor permite la vinculación a sus objetos incrustados, debe registrar un CLSID para cada clase de objetos admitida.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CLSID registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854985"
---
# <a name="clsid-key"></a>Clave CLSID

Un CLSID es un identificador único global que identifica un objeto de clase COM. Si el servidor o contenedor permite la vinculación a sus objetos incrustados, debe registrar un CLSID para cada clase de objetos admitida.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Clases DE SOFTWARE DE MÁQUINA LOCAL \_ \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Clave del Registro                                                 | Descripción                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid.md)                                       | Asocia un AppID a un CLSID.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos .                                                |
| [**AutoTreatAs**](autotreatas.md)                           | Establece automáticamente el CLSID de la clave [**TreatAs**](treatas.md) en el valor especificado.                                              |
| [**AuxUserType**](auxusertype.md)                           | Especifica el nombre para mostrar corto de una aplicación y los nombres de aplicación.                                                                     |
| [**Control**](control.md)                                   | Identifica un objeto como un control ActiveX control.                                                                                              |
| [**Conversión**](conversion.md)                             | Usado por el **cuadro de** diálogo Convertir para determinar los formatos que una aplicación puede leer y escribir.                                           |
| [**DataFormats**](dataformats.md)                           | Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Proporciona información de iconos predeterminada para presentaciones iónicas de objetos.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Especifica si una aplicación usa un controlador personalizado.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Especifica si una aplicación usa un controlador personalizado.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Especifica la ruta de acceso al archivo DLL del servidor en proceso.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.                           |
| [**Insertable**](insertable.md)                             | Indica que los objetos de esta clase deben aparecer en el cuadro de lista Cuadro de **diálogo Insertar** objeto cuando lo usan las aplicaciones de contenedor COM. |
| [**Interfaz**](interface.md)                               | Entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.                                             |
| [**LocalServer**](localserver.md)                           | Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Especifica cómo crear y mostrar un objeto .                                                                                           |
| [**ProgID**](progid.md)                                     | Asocia un ProgID a un CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica el nombre del módulo y el identificador de recurso de un mapa de bits de 16 x 16 que se usará para la cara de un botón de barra de herramientas o cuadro de herramientas.                      |
| [**TreatAs**](treatas.md)                                   | Especifica el CLSID de una clase que puede emular la clase actual.                                                                       |
| [**Verbo**](verb.md)                                         | Especifica los verbos que se registrarán para una aplicación.                                                                                 |
| [**Versión**](version.md)                                   | Especifica el número de versión del control.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Asocia un ProgID a un CLSID. Este valor se usa para determinar la versión más reciente de una aplicación de objeto.                           |



 

## <a name="remarks"></a>Comentarios

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

La clave CLSID contiene información utilizada por el controlador COM predeterminado para devolver información sobre una clase cuando está en estado de ejecución.

Para obtener un CLSID para la aplicación, puede usar el Uuidgen.exe o usar la [**función CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)

CLSID es un número de 128 bits, en hexadecimal, dentro de un par de llaves.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




