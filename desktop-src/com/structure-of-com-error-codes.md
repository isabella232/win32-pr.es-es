---
title: Estructura de los códigos de error COM
description: Estructura de los códigos de error COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104560789"
---
# <a name="structure-of-com-error-codes"></a>Estructura de los códigos de error COM

En la ilustración siguiente se muestra el formato de un [**valor HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (o SCODE); los números indican las posiciones de bits:

![Muestra el formato de un "resultado H" o del código "con números que indican las posiciones de los bits.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

El bit de orden superior de **HRESULT** o SCODE indica si el valor devuelto representa el éxito o el error. Si se establece en 0, SEVERity \_ Success, el valor indica Success. Si se establece en 1, \_ error de gravedad, indica un error.

Los bits R, C, N y r están reservados.

El campo Facility indica el servicio de sistema responsable del error. Microsoft asigna nuevos códigos de instalaciones a medida que son necesarios. La mayoría de los valores SCODEs y **HRESULT** establecen el campo Facility en facil \_ ITF, que indica un error del método de interfaz.

Los campos de instalación comunes se describen en la tabla siguiente.



| Campo de instalación                | Value        | Descripción                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| distribución de instalaciones \_<br/> | 2<br/> | Para los errores de interfaz **IDispatch** de enlace en tiempo de ejecución. <br/>                                                                                                                                                                                                                                                             |
| INSTALACIÓN de \_ ITF<br/>      | 4<br/> | Para la mayoría de los códigos de estado devueltos por los métodos de interfaz. El significado real del error se define mediante la interfaz. Es decir, dos valores **HRESULT** con exactamente el mismo valor de 32 bits devueltos de dos interfaces diferentes pueden tener significados diferentes. <br/>                                                       |
| CAPACIDAD \_ nula<br/>     | 0<br/> | Para los códigos de estado comunes de gran aplicación, como es \_ correcto. <br/>                                                                                                                                                                                                                                                    |
| SERVICIO \_ RPC<br/>      | 1<br/> | Para los códigos de estado devueltos por las llamadas a procedimiento remoto. <br/>                                                                                                                                                                                                                                                       |
| almacenamiento de instalaciones \_<br/>  | 3<br/> | Para los códigos de estado devueltos por las llamadas a métodos [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relacionadas con el almacenamiento estructurado. Los códigos de Estado cuyo valor de código (menor de 16 bits) está en el intervalo de códigos de error de MS-DOS (es decir, menor que 256) tienen el mismo significado que el error de MS-DOS correspondiente. <br/> |
| INSTALACIÓN de \_ Win32<br/>    | 7<br/> | Se usa para proporcionar un medio para controlar los códigos de error de las funciones de la API de Windows como **HRESULT**. Los códigos de error en OLE de 16 bits que los códigos de error del sistema duplicados también se han cambiado a la característica \_ Win32. <br/>                                                                                                 |
| ventanas de instalaciones \_<br/>  | 8<br/> | Se usa para otros códigos de error de las interfaces definidas por Microsoft.<br/>                                                                                                                                                                                                                                            |



 

El campo de código es un número único que se asigna para representar el error o la advertencia.

Por Convención, los valores **HRESULT** suelen tener nombres con el siguiente formato: razón de gravedad de la *utilidad* \_  \_ .

*Facility* es el nombre de la instalación o algún otro identificador distintivo; *Severity* es una sola letra, S o E, que indica si la llamada a la función se realizó correctamente o produjo un error (E); y *Reason* es un identificador que describe el significado del código. Por ejemplo, el código de estado STG \_ E \_ FILENOTFOUND indica que se ha producido un error relacionado con el almacenamiento; en concreto, el archivo solicitado no existe. Los códigos de estado de \_ la función null omiten el prefijo de la *utilidad* \_ .

Los códigos de error se definen en el contexto de una implementación de interfaz. Una vez definidos, los códigos de éxito no se pueden cambiar o se agregan nuevos códigos de éxito. Sin embargo, se pueden escribir nuevos códigos de error. Microsoft se reserva el derecho de definir nuevos códigos de error (pero no códigos correctos) para las interfaces descritas en facil \_ ITF o en nuevas instalaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> <dt>

[Protocolos de Windows: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

