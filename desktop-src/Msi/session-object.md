---
description: El objeto Session controla el proceso de instalación.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Objeto Session (Windows Installer)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272484"
---
# <a name="session-object-windows-installer"></a>Objeto Session (Windows Installer)

El **objeto Session** controla el proceso de instalación. Se abre la base de datos installer, que contiene los datos y las tablas de instalación. Este objeto está asociado a un conjunto estándar de funciones de acción, cada una de las que realiza operaciones concretas en datos de una o varias tablas. Se pueden agregar acciones personalizadas adicionales para instalaciones de productos concretas. La función básica del motor es un secuenciador que captura registros secuenciales de una tabla de secuencias designada, evalúa cualquier expresión de condición especificada y ejecuta la acción designada. Las acciones no reconocidas por el motor se aplazan al objeto de controlador de interfaz de usuario para su procesamiento, normalmente secuencias de cuadro de diálogo.

Tenga en cuenta que solo un **proceso** puede abrir un objeto Session.

## <a name="members"></a>Members

El **objeto Session** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Session** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Ejecuta la acción especificada. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Evalúa una expresión lógica que contiene símbolos y valores y devuelve un entero de la enumeración msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Devuelve un [**objeto FeatureInfo**](featureinfo-object.md) que contiene información descriptiva para la característica especificada.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Devuelve una cadena con formato a partir de datos de plantilla y registro.<br/>                                                                                                                                                                                                      |
| [**Mensaje**](session-message.md)                     | Realiza las operaciones de registro habilitadas y aplaza la ejecución al objeto de controlador de interfaz de usuario asociado al motor.<br/>                                                                                                                                              |
| [**Secuencia**](session-sequence.md)                   | Abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Secuencia. Para cada fila capturada, se llama al [**método DoAction,**](session-doaction.md) siempre que cualquier expresión de condición proporcionada no se evalúe como False.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los estados Select e Installed para todas las características.<br/>                                                                                                                    |



 

### <a name="properties"></a>Propiedades

El **objeto Session** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso           | Descripción                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Devuelve un [**objeto RecordList**](recordlist-object.md) que enumera el espacio en disco por unidad necesario para instalar un componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Devuelve el estado instalado actual del componente designado.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Obtiene o solicita un cambio en el estado Acción de una fila de la tabla Componente.<br/>                                                                               |
| [**Base de datos**](session-database.md)<br/>                           |                       | Devuelve la base de datos de la sesión de instalación actual.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características primarias (hasta la raíz de la tabla Característica).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Devuelve el estado instalado actual de la característica designada.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lectura y escritura<br/> | Obtiene o solicita un cambio en el estado Select de los registros y subrecords de una característica.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Devuelve un entero que representa marcas de bits con cada bit pertinente que representa un estado de instalación válido para la característica especificada.<br/>                             |
| [**Instalador**](session-installer.md)<br/>                         |                       | Devuelve el objeto del instalador activo.<br/>                                                                                                                            |
| [**Language (objeto session)**](session-language.md)<br/>          |                       | Representa el identificador de idioma numérico utilizado por la sesión de instalación actual.<br/>                                                                            |
| [**Modo**](session-mode.md)<br/>                                   |                       | Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Representa el valor de cadena de una propiedad de instalador con nombre.<br/>                                                                                                      |
| [**Propiedad (objeto Session)**](session-session.md)<br/>           | Lectura y escritura<br/> | Recupera las propiedades del producto de la base de datos del producto.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lectura y escritura<br/> | Proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de instalación.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Devuelve true si existe suficiente espacio en disco y false si el disco está lleno.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




