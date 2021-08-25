---
title: Opciones del compilador MIDL
description: Opciones del compilador MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649cd96ffc0afa171ad218a737910ce15facbe0e9b5ef302dedb6615228bcf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859335"
---
# <a name="midl-compiler-options"></a>Opciones del compilador MIDL

Puede usar las siguientes opciones de línea de comandos para invalidar parte del comportamiento predeterminado del compilador midl y para elegir las optimizaciones adecuadas para la aplicación. Para obtener una lista completa de las opciones de la línea de comandos de MIDL, vea [midl Command-Line referencia](/windows/desktop/Midl/midl-command-line-reference).



| Modificador de la línea de comandos                                       | Descripción                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Use para proporcionar un nombre de archivo ACF explícito. Este modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Especifica un nombre de archivo para el archivo de datos DLL generado para un archivo DLL de proxy. El nombre de archivo predeterminado es Dlldata.c.<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | Dirige a MIDL para generar códigos auxiliares o una biblioteca de tipos para un entorno de destino.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Especifica el nombre del archivo de encabezado de interfaz. El nombre predeterminado es el del archivo IDL con una extensión .h.<br/>                                                                                                                       |
| [**/iid**](/windows/desktop/Midl/-iid)<br/>                          | Especifica un nombre de archivo de identificador de interfaz que invalida el nombre de archivo del identificador de interfaz predeterminado para una interfaz COM.<br/>                                                                                                              |
| [**/lcid**](/windows/desktop/Midl/-lcid)<br/>                        | Proporciona compatibilidad completa con DBCS para que pueda usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.<br/>                                                                                                          |
| [**/no \_ format \_ opt**](/windows/desktop/Midl/-no-format-opt)<br/>    | De forma predeterminada, para reducir el tamaño del código, MIDL elimina los descriptores duplicados. Este modificador desactiva este comportamiento de optimización.<br/>                                                                                                               |
| [**/Oi**](/windows/desktop/Midl/-oi), **/Oic**, **/Oif**<br/>        | Ordena a MIDL que use un método de serialización totalmente interpretado. Los modificadores /Oic y /Oicf proporcionan mejoras de rendimiento adicionales.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Especifica el directorio en el que el compilador MIDL escribe los archivos de salida. El directorio de salida se puede especificar con una letra de unidad, un nombre de ruta de acceso absoluto o ambos. El valor predeterminado es que MIDL escribe los archivos en el directorio actual.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Especifica el nombre del archivo de proxy de interfaz para una interfaz COM. El nombre predeterminado es el del archivo IDL más \_ "p.c".<br/>                                                                                                            |
| [**/tlb**](/windows/desktop/Midl/-tlb)<br/>                          | Especifica el nombre del archivo de biblioteca de tipos. El nombre predeterminado es el del archivo IDL, con una extensión .tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilación midl](midl-compilation.md)
</dt> </dl>

 

