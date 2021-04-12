---
title: Estrategias de control de errores
description: Estrategias de control de errores
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104487267"
---
# <a name="error-handling-strategies"></a>Estrategias de control de errores

Dado que los métodos de interfaz son virtuales, no es posible que un llamador conozca el conjunto completo de valores que se pueden devolver desde cualquier llamada. Una implementación de un método puede devolver cinco valores; otro puede devolver ocho.

En la documentación se enumeran los valores comunes que se pueden devolver para cada método; Estos son los valores que debe comprobar y controlar en el código porque tienen significados especiales. Se pueden devolver otros valores, pero dado que no son significativos, no es necesario escribir código especial para controlarlos. Una comprobación simple para cero o un valor distinto de cero es adecuada.

## <a name="hresult-values"></a>Valores HRESULT

El valor devuelto de los métodos y funciones COM es **HRESULT**. Los valores de algunos HRESULTs se han cambiado en COM para eliminar toda la duplicación y superponerse con los códigos de error del sistema. Los códigos de error del sistema duplicados se han cambiado a la característica \_ Win32 y los que se superponen permanecen en el \_ valor null. En la tabla siguiente se enumeran los valores **HRESULT** comunes y sus valores.



| HRESULT                    | Value                 | Descripción                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ anular<br/>        | 0x80004004<br/> | La operación se anuló debido a un error no especificado.<br/>                                                                              |
| E \_ ACCESSDENIED<br/> | 0x80070005<br/> | Un error general de acceso denegado.<br/>                                                                                                          |
| E \_ FAIL<br/>         | 0x80004005<br/> | Se ha producido un error no especificado.<br/>                                                                                                    |
| \_identificador E<br/>       | 0x80070006<br/> | Se usó un identificador no válido.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Uno o varios argumentos no son válidos.<br/>                                                                                                      |
| E \_ NOinterface<br/>  | 0x80004002<br/> | El método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no reconoció la interfaz solicitada. No se admite la interfaz.<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | El método no está implementado.<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | El método no pudo asignar la memoria necesaria.<br/>                                                                                         |
| E \_ pendientes<br/>      | 0x8000000A<br/> | Los datos necesarios para completar la operación aún no están disponibles.<br/>                                                                      |
| \_puntero E<br/>      | 0x80004003<br/> | Se usó un puntero no válido.<br/>                                                                                                            |
| E \_ inesperado<br/>   | 0x8000FFFF<br/> | Se ha producido un error catastrófico.<br/>                                                                                                    |
| S \_ false<br/>        | 0x00000001<br/> | El método se ejecutó correctamente y devolvió el valor booleano **false**.<br/>                                                                          |
| S \_ correcto<br/>           | 0x00000000<br/> | El método se ha llevado a cabo de forma correcta. Si se espera un valor devuelto booleano, el valor devuelto es **true**.<br/>                                            |



 

## <a name="network-errors"></a>Errores de red

Si los cuatro primeros dígitos del código de error son 8007, indica un error del sistema o de la red. Puede usar el comando **net** para descodificar estos tipos de errores. Para descodificar el error, convierta primero los cuatro últimos dígitos del código de error hexadecimal a decimal. A continuación, en el símbolo del sistema, escriba lo siguiente, donde el código decimal se reemplaza por el valor devuelto que desea descodificar:

**net helpmsg <***\_ código decimal***>**

El comando net devuelve una descripción del error. Por ejemplo, si COM devuelve el error 8007054B, convierta 054B en decimal (1355). A continuación, escriba lo siguiente:

**net helpmsg 1355**

El comando net devuelve la descripción del error: "el dominio especificado no existía".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

 





