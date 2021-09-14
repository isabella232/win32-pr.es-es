---
title: Estructura de códigos de error COM
description: Estructura de códigos de error COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253178"
---
# <a name="structure-of-com-error-codes"></a>Estructura de códigos de error COM

En la ilustración siguiente se muestra el formato de [**un valor HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (o SCODE); los números indican posiciones de bits:

![Muestra el formato de "H RESULT" o "S CODE" con números que indican posiciones de bits.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

El bit de orden superior en **HRESULT** o SCODE indica si el valor devuelto representa un éxito o un error. Si se establece en 0, SEVERITY \_ SUCCESS, el valor indica que se ha hecho correctamente. Si se establece en 1, ERROR DE \_ GRAVEDAD, indica un error.

Los bits R, C, N y r están reservados.

El campo de instalación indica el servicio del sistema responsable del error. Microsoft asigna nuevos códigos de instalación a medida que sean necesarios. La mayoría de los valores SCODEs y **HRESULT** establecen el campo facility en FACILITY \_ ITF, lo que indica un error del método de interfaz.

Los campos de instalación comunes se describen en la tabla siguiente.



| Campo De instalación                | Value        | Descripción                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DISTRIBUCIÓN \_ DE LA INSTALACIÓN<br/> | 2<br/> | Para errores de la **interfaz IDispatch de** enlace en tiempo de ejecución. <br/>                                                                                                                                                                                                                                                             |
| ITF \_ DE LA INSTALACIÓN<br/>      | 4<br/> | Para la mayoría de los códigos de estado devueltos desde métodos de interfaz. La interfaz define el significado real del error. Es decir, dos **HRESULT** con exactamente el mismo valor de 32 bits devuelto desde dos interfaces diferentes pueden tener significados diferentes. <br/>                                                       |
| FACILITY \_ NULL<br/>     | 0<br/> | Para códigos de estado comunes ampliamente aplicables, como S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| RPC \_ DE INSTALACIÓN<br/>      | 1<br/> | Para los códigos de estado devueltos por las llamadas a procedimiento remoto. <br/>                                                                                                                                                                                                                                                       |
| ALMACENAMIENTO DE \_ LA INSTALACIÓN<br/>  | 3<br/> | Para los códigos de estado devueltos por llamadas al método [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relacionadas con el almacenamiento estructurado. Los códigos de estado cuyo valor de código (16 bits inferior) se encuentra en el intervalo de códigos de error de MS-DOS (es decir, menos de 256) tienen el mismo significado que el error MS-DOS correspondiente. <br/> |
| FACILITY \_ WIN32<br/>    | 7<br/> | Se usa para proporcionar un medio para controlar los códigos de error de las funciones de Windows API como **HRESULT**. Los códigos de error de OLE de 16 bits que duplican los códigos de error del sistema también se han cambiado a FACILITY \_ WIN32. <br/>                                                                                                 |
| VENTANAS DE \_ INSTALACIÓN<br/>  | 8<br/> | Se usa para códigos de error adicionales de interfaces definidas por Microsoft.<br/>                                                                                                                                                                                                                                            |



 

El campo de código es un número único que se asigna para representar el error o la advertencia.

Por convención, **los valores HRESULT** suelen tener nombres con el formato siguiente: *Motivo de* gravedad de \_ *la* \_ *instalación.*

*La* instalación es el nombre de la instalación o algún otro identificador distintivo; *La gravedad* es una sola letra, S o E, que indica si la llamada a la función se ha producido correctamente (S) o si se ha producido un error (E); y *Reason* es un identificador que describe el significado del código. Por ejemplo, el código de estado STG E FILENOTFOUND indica que se ha producido un error relacionado con el almacenamiento; en concreto, no existe un archivo \_ \_ solicitado. Los códigos de estado de FACILITY \_ NULL omiten el *prefijo Facility.* \_

Los códigos de error se definen en el contexto de una implementación de interfaz. Una vez definidos, no se pueden cambiar los códigos de éxito ni agregar nuevos códigos de éxito. Sin embargo, se pueden escribir nuevos códigos de error. Microsoft se reserva el derecho de definir nuevos códigos de error (pero no códigos de éxito) para las interfaces descritas en FACILITY ITF o \_ en nuevas instalaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> <dt>

[Windows Protocolos: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

