---
description: El objeto de sesión controla el proceso de instalación.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653976"
---
# <a name="session-object-windows-installer"></a>Objeto Session (Windows Installer)

El objeto de **sesión** controla el proceso de instalación. Se abre la base de datos del instalador, que contiene las tablas y los datos de instalación. Este objeto está asociado a un conjunto estándar de funciones de acción, cada una de las cuales realiza operaciones particulares en los datos de una o más tablas. Se pueden agregar acciones personalizadas adicionales para instalaciones de productos determinadas. La función básica Engine es un secuenciador que captura registros secuenciales de una tabla de secuencia designada, evalúa cualquier expresión de condición especificada y ejecuta la acción designada. Las acciones no reconocidas por el motor se difieren al objeto de controlador de interfaz de usuario para el procesamiento, normalmente secuencias de cuadros de diálogo.

Tenga en cuenta que solo un único proceso puede abrir un objeto de **sesión** .

## <a name="members"></a>Miembros

El objeto de **sesión** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **sesión** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Ejecuta la acción especificada. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Evalúa una expresión lógica que contiene símbolos y valores y devuelve un entero de la enumeración msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Devuelve un objeto [**FeatureInfo**](featureinfo-object.md) que contiene información descriptiva de la característica especificada.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Devuelve una cadena con formato de los datos de la plantilla y del registro.<br/>                                                                                                                                                                                                      |
| [**Message**](session-message.md)                     | Realiza cualquier operación de registro habilitada y pospone la ejecución al objeto de controlador de interfaz de usuario asociado al motor.<br/>                                                                                                                                              |
| [**SPRJ**](session-sequence.md)                   | Abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna de secuencia. Para cada fila capturada, se llama al método [**OnAction**](session-doaction.md) , siempre que cualquier expresión de condición proporcionada no se evalúe como false.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los Estados SELECT y installed para todas las características.<br/>                                                                                                                    |



 

### <a name="properties"></a>Propiedades

El objeto de **sesión** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso           | Descripción                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Devuelve un objeto [**RecordList**](recordlist-object.md) que enumera el espacio en disco por unidad necesaria para instalar un componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Devuelve el estado instalado actual del componente designado.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Obtiene o solicita un cambio en el estado de acción de una fila de la tabla de componentes.<br/>                                                                               |
| [**Base de datos**](session-database.md)<br/>                           |                       | Devuelve la base de datos de la sesión de instalación actual.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características principales (hasta la raíz de la tabla de características).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Devuelve el estado instalado actual de la característica designada.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lectura/escritura<br/> | Obtiene o solicita un cambio en el estado de selección del registro y los subregistros de una característica.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Devuelve un entero que representa las marcas de bits con cada bit pertinente que representa un estado de instalación válido de la característica especificada.<br/>                             |
| [**Instalador**](session-installer.md)<br/>                         |                       | Devuelve el objeto de instalador activo.<br/>                                                                                                                            |
| [**Language (objeto de sesión)**](session-language.md)<br/>          |                       | Representa el identificador de idioma numérico utilizado por la sesión de instalación actual.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Representa el valor de cadena de una propiedad de instalador con nombre.<br/>                                                                                                      |
| [**Property (objeto de sesión)**](session-session.md)<br/>           | Lectura/escritura<br/> | Recupera las propiedades del producto de la base de datos del producto.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lectura/escritura<br/> | Proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de la instalación.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Devuelve true si existe suficiente espacio en disco y false si el disco está lleno.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




