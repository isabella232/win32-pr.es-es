---
title: Opciones del compilador de MIDL
description: Opciones del compilador de MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e219daa345ad3140b78db8fdfc3de1d28678120
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359450"
---
# <a name="midl-compiler-options"></a>Opciones del compilador de MIDL

Puede utilizar las siguientes opciones de línea de comandos para invalidar parte del comportamiento predeterminado del compilador de MIDL y elegir las optimizaciones adecuadas para la aplicación. Para obtener una lista completa de las opciones de línea de comandos de MIDL, vea la [referencia de midl Command-Line](/windows/desktop/Midl/midl-command-line-reference).



| Modificador de la línea de comandos                                       | Descripción                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Se usa para proporcionar un nombre de archivo ACF explícito. Este modificador también habilita el uso de diferentes nombres de interfaz en los archivos IDL y ACF.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Especifica un nombre de archivo para el archivo de datos DLL generado para un archivo DLL de proxy. El nombre de archivo predeterminado es dlldata. c.<br/>                                                                                                                              |
| [**/ENV**](/windows/desktop/Midl/-env)<br/>                          | Indica a MIDL que genere códigos auxiliares o una biblioteca de tipos para un entorno de destino.<br/>                                                                                                                                                            |
| [**/Header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Especifica el nombre del archivo de encabezado de interfaz. El nombre predeterminado es el del archivo IDL con la extensión. h.<br/>                                                                                                                       |
| [**/IID**](/windows/desktop/Midl/-iid)<br/>                          | Especifica un identificador de interfaz de archivo que invalida el nombre de archivo del identificador de interfaz predeterminado para una interfaz COM.<br/>                                                                                                              |
| [**/LCID**](/windows/desktop/Midl/-lcid)<br/>                        | Proporciona compatibilidad completa con DBCS para que pueda usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.<br/>                                                                                                          |
| [**/no \_ format \_ OPC**](/windows/desktop/Midl/-no-format-opt)<br/>    | De forma predeterminada, para reducir el tamaño del código, MIDL elimina los descriptores duplicados. Este modificador desactiva este comportamiento de optimización.<br/>                                                                                                               |
| [**/OI**](/windows/desktop/Midl/-oi), **/OIC**, **/OIF**<br/>        | Indica a MIDL que use un método de cálculo de referencias completamente interpretado. Los conmutadores/OIC y/Oicf proporcionan mejoras de rendimiento adicionales.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Especifica el directorio en el que el compilador MIDL escribe los archivos de salida. El directorio de salida se puede especificar con una letra de unidad, un nombreruta absoluto o ambos. El valor predeterminado es que MIDL escribe los archivos en el directorio actual.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Especifica el nombre del archivo de proxy de interfaz para una interfaz COM. El nombre predeterminado es el del archivo IDL más " \_ p. c".<br/>                                                                                                            |
| [**/TLB**](/windows/desktop/Midl/-tlb)<br/>                          | Especifica el nombre del archivo de biblioteca de tipos. El nombre predeterminado es el del archivo IDL, con una extensión. tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilación de MIDL](midl-compilation.md)
</dt> </dl>

 

